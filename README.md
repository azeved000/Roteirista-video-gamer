# 🎮 Roteirista de Vídeos Gamer com IA

Sistema automatizado de criação de roteiros e thumbnails para vídeos de jogos no YouTube usando agentes de IA com CrewAI.

## 📋 Descrição

Este projeto utiliza múltiplos agentes de IA especializados para automatizar o processo completo de criação de conteúdo para YouTube no nicho gamer. O sistema gera roteiros detalhados, cria opções de thumbnails e revisa todo o conteúdo, entregando um pacote de produção completo e pronto para uso.

## 🤖 Agentes de IA

O sistema é composto por 3 agentes especializados:

### 1. Roteirista de Vídeos Gamer
- Pesquisa informações atualizadas sobre o tema
- Elabora roteiros detalhados e envolventes
- Estrutura o conteúdo com introdução, desenvolvimento e conclusão
- Sugere elementos visuais e timing para cada seção

### 2. Designer de Thumbnails
- Cria 3 opções distintas de thumbnails
- Define paletas de cores vibrantes
- Especifica textos impactantes
- Analisa e escolhe a melhor opção baseado em CTR potencial

### 3. Revisor de Conteúdo
- Revisa e consolida roteiro e thumbnail
- Corrige erros e melhora a fluidez
- Gera documento final pronto para produção

## 🚀 Funcionalidades

- ✅ Geração automática de roteiros completos para YouTube
- ✅ Criação de 3 opções de thumbnails com análise detalhada
- ✅ Pesquisa web integrada para informações atualizadas
- ✅ Revisão e consolidação de todo o conteúdo
- ✅ Documento final formatado e pronto para produção

## 🛠️ Tecnologias

- **CrewAI**: Framework para orquestração de agentes de IA
- **OpenAI GPT-4**: Modelo de linguagem para os agentes
- **LangChain**: Ferramentas para integração com LLMs
- **DuckDuckGo Search**: Ferramenta de pesquisa web
- **Python 3.x**: Linguagem principal
- **Jupyter Notebook**: Ambiente de desenvolvimento

## 📦 Instalação

1. Clone o repositório:
```bash
git clone https://github.com/azeved000/Roteirista-video-gamer.git
cd Roteirista-video-gamer
```

2. Instale as dependências:
```bash
pip install crewai langchain langchain-openai langchain-community markdown
```

3. Configure sua chave da OpenAI:
```python
os.environ["OPENAI_API_KEY"] = "sua-chave-aqui"
```

## 💻 Como Usar

1. Abra o notebook `roteirogamer.ipynb`

2. Execute as células de configuração (importações e configuração de API)

3. Execute a criação dos agentes e tarefas

4. Execute o crew com seu tema:
```python
result = crew.kickoff(inputs={'query': 'Seu tema aqui'})
```

5. Visualize o resultado final:
```python
from IPython.display import Markdown
Markdown(result.raw)
```

## 📄 Estrutura do Projeto

```
Roteirista-video-gamer/
│
├── roteirogamer.ipynb      # Notebook principal com todo o sistema
└── README.md               # Este arquivo
```

## 🎯 Exemplo de Uso

```python
# Executar o sistema para criar conteúdo sobre "Melhores jogos de 2020"
result = crew.kickoff(inputs={'query': 'Melhores jogos de 2020'})

# Ver o pacote completo de produção
Markdown(result.raw)

# Ver apenas as 3 opções de thumbnails
Markdown(criar_thumbnails.output.raw)
```

## 📊 Output Gerado

O sistema gera um documento completo contendo:

- 📋 Informações do projeto (tema, duração, público-alvo)
- 🎬 Roteiro completo do vídeo (introdução, desenvolvimento, conclusão)
- 🎨 3 opções de thumbnails detalhadas
- ✅ Thumbnail escolhida com justificativa
- 📝 Checklist de produção
- 💡 Notas da revisão

## 🔧 Personalização

Você pode personalizar:

- **Modelos**: Alterar o modelo GPT usado (`gpt-4o`, `gpt-4-turbo`, etc.)
- **Agentes**: Modificar roles, goals e backstories
- **Tarefas**: Ajustar descrições e expected_output
- **Ferramentas**: Adicionar novas ferramentas de pesquisa ou análise

## 📝 Licença

Este projeto é de código aberto e está disponível para uso educacional e comercial.

## 👤 Autor

**azeved000**

- GitHub: [@azeved000](https://github.com/azeved000)

## 🤝 Contribuições

Contribuições, issues e feature requests são bem-vindos!

## ⭐ Mostre seu apoio

Se este projeto foi útil, considere dar uma ⭐!

---

**Desenvolvido com ❤️ usando CrewAI e OpenAI**
