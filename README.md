# 🚀 Primeiros Projetos - Jornada de Aprendizado

Bem-vindo ao meu repositório de aprendizado! Aqui documento meus primeiros passos na programação enquanto estudo para o ENEM e me preparo para a carreira em tecnologia.

<div align="center">
  
  ![GitHub last commit](https://img.shields.io/github/last-commit/Luke08theman/primeiros-projetos)
  ![GitHub repo size](https://img.shields.io/github/repo-size/Luke08theman/primeiros-projetos)
  ![GitHub language count](https://img.shields.io/github/languages/count/Luke08theman/primeiros-projetos)
  
</div>

## 👨‍💻 Sobre Mim

Sou Lucas Cancio, estudante de **Automação Industrial no IFMG** (3º ano). Estou aprendendo programação de forma autodidata enquanto me preparo para entrar em **Sistemas de Informação**.

**Idiomas:** Português (nativo), Inglês (B2), Espanhol (B2)  
**Objetivo:** Desenvolvedor Full Stack + Aposentadoria aos 40 anos 🎯

---

## 📚 O Que Você Vai Encontrar Aqui

Este repositório contém projetos simples mas funcionais que desenvolvi durante meu aprendizado. Cada projeto representa uma nova habilidade adquirida.

### Projetos Disponíveis:

| # | Projeto | Descrição | Tecnologias | Status |
|---|---------|-----------|-------------|--------|
| 01 | [Formulário Multilíngue](#01-formulário-multilíngue) | Sistema de apresentação em 3 idiomas | Python | ✅ Completo |
| 02 | [Calculadora Simples](#02-calculadora-simples) | Calculadora com operações básicas | Python | ✅ Completo |
| 03 | [Gerador de Senhas](#03-gerador-de-senhas) | Cria senhas fortes aleatórias | Python | 🔄 Em progresso |
| 04 | [To-Do List CLI](#04-to-do-list-cli) | Lista de tarefas no terminal | Python | 📝 Planejado |

> 💡 **Nota:** Estou focando em Python primeiro, depois vou para JavaScript e desenvolvimento web.

---

## 🎯 Projetos Detalhados

### 01. Formulário Multilíngue

**O que faz:** Coleta nome, idade, país e idioma do usuário, depois exibe uma mensagem personalizada no idioma escolhido (Português, Inglês ou Espanhol).

**Habilidades praticadas:**
- ✅ Input/Output
- ✅ Condicionais (if/elif/else)
- ✅ Manipulação de strings
- ✅ Dicionários Python
- ✅ Internacionalização básica

**Como executar:**
```bashcd formulario-multilingue
python main.py

**Exemplo de uso:**=== FORMULÁRIO DE APRESENTAÇÃO ===
Nome: Lucas
Idade: 17
País: Brasil
Idioma (pt/en/es): ptOlá Lucas! Você tem 17 anos e mora no Brasil.
Bem-vindo! 🇧🇷

**Código:**
```pythonformulario-multilingue/main.pydef coletar_dados():
"""Coleta informações do usuário"""
print("=== FORMULÁRIO DE APRESENTAÇÃO ===")
nome = input("Nome: ")
idade = int(input("Idade: "))
pais = input("País: ")
idioma = input("Idioma (pt/en/es): ").lower()return nome, idade, pais, idiomadef gerar_mensagem(nome, idade, pais, idioma):
"""Gera mensagem personalizada no idioma escolhido"""# Dicionário com mensagens em cada idioma
mensagens = {
    'pt': f"Olá {nome}! Você tem {idade} anos e mora em/no {pais}. Bem-vindo! 🇧🇷",
    'en': f"Hello {nome}! You are {idade} years old and live in {pais}. Welcome! 🇺🇸",
    'es': f"¡Hola {nome}! Tienes {idade} años y vives en {pais}. ¡Bienvenido! 🇪🇸"
}# Retorna mensagem ou mensagem padrão se idioma inválido
return mensagens.get(idioma, mensagens['pt'])def main():
"""Função principal"""
nome, idade, pais, idioma = coletar_dados()
mensagem = gerar_mensagem(nome, idade, pais, idioma)
print(f"\n{mensagem}")if name == "main":
main()

**O que aprendi:**
- Como estruturar um programa Python com funções
- Trabalhar com entrada de dados e validação básica
- Usar dicionários para organizar dados
- Implementar suporte a múltiplos idiomas
- Boas práticas: docstrings, if __name__ == "__main__"

**Melhorias futuras:**
- [ ] Adicionar validação de idade (não aceitar números negativos)
- [ ] Salvar dados em arquivo JSON
- [ ] Adicionar mais idiomas
- [ ] Criar interface gráfica (Tkinter)

---

### 02. Calculadora Simples

**O que faz:** Realiza operações matemáticas básicas (+, -, *, /) via terminal.

**Habilidades praticadas:**
- ✅ Funções
- ✅ Tratamento de exceções (try/except)
- ✅ While loops
- ✅ Operadores matemáticos
- ✅ Validação de input

**Como executar:**
```bashcd calculadora-simples
python calculadora.py

**Código:**
```pythoncalculadora-simples/calculadora.pydef somar(a, b):
"""Soma dois números"""
return a + bdef subtrair(a, b):
"""Subtrai b de a"""
return a - bdef multiplicar(a, b):
"""Multiplica dois números"""
return a * bdef dividir(a, b):
"""Divide a por b (com tratamento de divisão por zero)"""
try:
return a / b
except ZeroDivisionError:
return "Erro: Divisão por zero não permitida!"def calculadora():
"""Loop principal da calculadora"""
print("=== CALCULADORA SIMPLES ===")
print("Operações: +, -, *, /")
print("Digite 'sair' para encerrar\n")while True:
    # Input do usuário
    operacao = input("Escolha a operação (+, -, *, /) ou 'sair': ")    if operacao.lower() == 'sair':
        print("Até logo!")
        break    if operacao not in ['+', '-', '*', '/']:
        print("❌ Operação inválida! Tente novamente.\n")
        continue    try:
        # Coleta os números
        num1 = float(input("Primeiro número: "))
        num2 = float(input("Segundo número: "))        # Executa operação
        if operacao == '+':
            resultado = somar(num1, num2)
        elif operacao == '-':
            resultado = subtrair(num1, num2)
        elif operacao == '*':
            resultado = multiplicar(num1, num2)
        elif operacao == '/':
            resultado = dividir(num1, num2)        print(f"\n✅ Resultado: {num1} {operacao} {num2} = {resultado}\n")    except ValueError:
        print("❌ Erro: Digite apenas números!\n")if name == "main":
calculadora()

**O que aprendi:**
- Tratamento de erros com try/except
- Como criar um loop interativo
- Validação de input do usuário
- Organização de código em funções pequenas e reutilizáveis

**Melhorias futuras:**
- [ ] Adicionar operações avançadas (potência, raiz, porcentagem)
- [ ] Histórico de cálculos
- [ ] Salvar histórico em arquivo
- [ ] Interface gráfica

---

### 03. Gerador de Senhas

**Status:** 🔄 Em desenvolvimento

**O que vai fazer:** Gerar senhas fortes e aleatórias com opções de personalização (tamanho, caracteres especiais, números).

**Objetivo de aprendizado:**
- Biblioteca `random`
- Biblioteca `string`
- Manipulação de listas
- Geração de números aleatórios

**Previsão de conclusão:** 1-2 semanas

---

## 🛠️ Tecnologias e Ferramentas

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

</div>

**Atualmente aprendendo:**
- Python (básico → intermediário)
- Lógica de programação
- Git/GitHub
- Estruturas de dados

**Próximos passos:**
- HTML/CSS/JavaScript
- Banco de dados (MySQL)
- Flask/Django (web com Python)

---

## 📈 Progresso de AprendizadoPython Básico       ████████████░░░░░░░░  60%
Git/GitHub          ████████░░░░░░░░░░░░  40%
Lógica Programação  ██████████░░░░░░░░░░  50%
HTML/CSS            ████░░░░░░░░░░░░░░░░  20%
JavaScript          ██░░░░░░░░░░░░░░░░░░  10%

**Meta atual:** Completar 10 projetos Python até Jul/2026

**Projetos concluídos:** 2/10

---

## 📝 Como Usar Este Repositório

### Pré-requisitos
- Python 3.8+ instalado
- Git instalado (opcional)

### Clonar o repositório
```bashgit clone https://github.com/Luke08theman/primeiros-projetos.git
cd primeiros-projetos

### Executar um projeto
```bashExemplo: Formulário Multilíngue
cd formulario-multilingue
python main.py

---

## 🎯 Objetivos de Aprendizado (2026)

- [x] Aprender sintaxe básica Python
- [x] Criar primeiro projeto funcional
- [x] Configurar Git/GitHub
- [ ] Completar 10 projetos Python
- [ ] Aprender HTML/CSS básico
- [ ] Aprender JavaScript básico
- [ ] Criar primeiro site
- [ ] Conseguir primeiro freela/estágio

---

## 🤝 Feedback e Sugestões

Sou iniciante e estou aprendendo! Se você é desenvolvedor experiente e tem sugestões de melhoria para meus projetos, ficarei muito grato:

- Abra uma [Issue](https://github.com/Luke08theman/primeiros-projetos/issues)
- Ou me mande uma mensagem no [LinkedIn](https://linkedin.com/in/lucas-cancio-soares-25a794221)

**Dúvidas comuns que já recebi:**
> "Por que Python e não JavaScript?"

Estou começando com Python porque a sintaxe é mais clara para iniciantes. Pretendo aprender JavaScript logo depois.

> "Vai fazer faculdade de quê?"

Meta é Sistemas de Informação (UFMG/UFV/UFSJ) a partir de 2027.

---

## 📚 Recursos que Estou Usando

**Cursos:**
- [Curso em Vídeo - Python](https://www.cursoemvideo.com/curso/python-3-mundo-1/) (Gustavo Guanabara)
- Code Combat (gamificação)
- Documentação oficial Python

**Livros:**
- "Automatize Tarefas Maçantes com Python" (Al Sweigart)
- "Python Fluente" (Luciano Ramalho) - futuro

**Comunidades:**
- Discord Python Brasil
- Stack Overflow (em inglês)

---

## 📊 Estatísticas do Repositório

![GitHub stats](https://github-readme-stats.vercel.app/api?username=Luke08theman&show_icons=true&theme=tokyonight)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Luke08theman&layout=compact&theme=tokyonight)

---

## 🗓️ Histórico de Updates

### Fevereiro 2026
- ✅ Criado repositório
- ✅ Primeiro projeto: Formulário Multilíngue
- ✅ Segundo projeto: Calculadora Simples

### Março 2026 (planejado)
- 🔄 Gerador de Senhas
- 🔄 To-Do List CLI
- 🔄 Início HTML/CSS

---

## 📄 Licença

Este projeto está sob a licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

---

## 📧 Contato

**Lucas Cancio Soares**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/lucas-cancio-soares-25a794221)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Luke08theman)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:l.canciosoares@gmail.com)

---

<div align="center">
  
  **⭐ Se este repositório te ajudou de alguma forma, considere dar uma estrela!**
  
  *"A jornada de mil milhas começa com um único passo." - Lao Tzu*
  
  ![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=Luke08theman.primeiros-projetos)
  
</div>
