import { useState } from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Menu, Search, BookOpen, FlaskConical, Youtube } from "lucide-react";

export default function HomePage() { const [articles] = useState([ { title: "A Física dos Buracos Negros", category: "Ciência", description: "Entenda os mistérios que envolvem esses monstros cósmicos...", }, { title: "Métodos de Estudo para ENEM", category: "Educação", description: "Aprenda técnicas de estudo que realmente funcionam...", }, { title: "Como o cérebro aprende?", category: "Neurociência", description: "A magia por trás da aprendizagem explicada cientificamente...", }, ]);

return ( <div className="min-h-screen bg-gray-100 text-gray-900"> <header className="bg-white shadow sticky top-0 z-50"> <div className="container mx-auto p-4 flex justify-between items-center"> <h1 className="text-2xl font-bold text-blue-600">EduCiência</h1> <nav className="space-x-4 hidden md:block"> <Button variant="ghost"><FlaskConical className="inline w-4 h-4 mr-1" />Ciência</Button> <Button variant="ghost"><BookOpen className="inline w-4 h-4 mr-1" />Educação</Button> <Button variant="ghost"><Youtube className="inline w-4 h-4 mr-1" />Vídeos</Button> <Button variant="ghost"><Search className="inline w-4 h-4 mr-1" />Buscar</Button> </nav> <Menu className="md:hidden" /> </div> </header>

<main className="container mx-auto p-4 grid md:grid-cols-2 lg:grid-cols-3 gap-6">
    {articles.map((article, i) => (
      <Card key={i} className="shadow-md hover:shadow-lg transition">
        <CardContent className="p-4">
          <h2 className="text-xl font-semibold mb-1">{article.title}</h2>
          <p className="text-sm text-blue-500 mb-2">{article.category}</p>
          <p className="text-gray-700 text-sm">{article.description}</p>
        </CardContent>
      </Card>
    ))}
  </main>

  <footer className="bg-blue-600 text-white text-center py-4 mt-10">
    <p>© 2025 EduCiência. Todos os direitos reservados.</p>
  </footer>
</div>

); }

## Hi there 👋

<!--
**Educiencia/educiencia** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
