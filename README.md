import os
estrutura = {
 
"src/main.jsx": """import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';
import './styles.css';
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
""",
 
"src/App.jsx": """import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
import Navbar from './components/Navbar';
import PaisAlunos from './pages/PaisAlunos';
import Apoio from './pages/Apoio';
import Supervisao from './pages/Supervisao';
import RecursosHumanos from './pages/RecursosHumanos';
import Projetos from './pages/Projetos';
function App() {
 return (
 
<Router>
 
<Navbar />
 
<div className="conteudo">
 
<Routes>
 
<Route path="/pais-alunos" element={<PaisAlunos />} />
 
<Route path="/apoio" element={<Apoio />} />
 
<Route path="/supervisao" element={<Supervisao />} />
 
<Route path="/rh" element={<RecursosHumanos />} />
 
<Route path="/projetos" element={<Projetos />} />
 
</Routes>
 
</div>
 
</Router>
 );
}
export default App;
""",
 
"src/components/Navbar.jsx": """import { Link } from 'react-router-dom';
export default function Navbar() {
 return (
 
<header className="navbar">
 
<nav>
 
<ul>
 
<li><Link to="/pais-alunos">Pais e Alunos</Link></li>
 
<li><Link to="/apoio">Apoio Pedagógico</Link></li>
 
<li><Link to="/supervisao">Supervisão</Link></li>
 
<li><Link to="/rh">RH</Link></li>
 
<li><Link to="/projetos">Projetos</Link></li>
 
</ul>
 
</nav>
 
</header>
 );
}""",
 
"src/pages/PaisAlunos.jsx": 'export default function PaisAlunos() { return <h2>Bem-vindo à área de Pais e Alunos</h2>; }',
 
"src/pages/Apoio.jsx": 'export default function Apoio() { return <h2>Recursos de Apoio Pedagógico</h2>; }',
 
"src/pages/Supervisao.jsx": 'export default function Supervisao() { return <h2>Área da Supervisão Escolar</h2>; }',
 
"src/pages/RecursosHumanos.jsx": 'export default function RecursosHumanos() { return <h2>Departamento de RH</h2>; }',
 
"src/pages/Projetos.jsx": 'export default function Projetos() { return <h2>Gerenciamento de Projetos Educacionais</h2>; }',
 
"src/styles.css": """body {
 margin: 0;
 font-family: 'Segoe UI', sans-serif;
 background-color: #f0f2f5;
}
.navbar {
 background-color: #2d6cdf;
 padding: 1rem;
}
.navbar ul {
 list-style: none;
 display: flex;
 gap: 1rem;
 margin: 0;
 padding: 0;
}
.navbar a {
 color: white;
 text-decoration: none;

}
.navbar a:hover {
 text-decoration: underline;
}
.conteudo {
 padding: 2rem;
}
""",# acti
