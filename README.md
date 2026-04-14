# Aula Docker - Projeto de Estudo

Este projeto é uma aplicação simples desenvolvida com Streamlit, containerizada usando Docker e implantada no Render. O objetivo principal é servir como material de estudo para aprender conceitos fundamentais de containerização com Docker e práticas de deploy em plataformas de nuvem como o Render.

## Descrição do Projeto

A aplicação é um "Hello World" básico em Streamlit, que exibe uma mensagem de boas-vindas. Embora simples, ela demonstra o fluxo completo de desenvolvimento, containerização e deploy de uma aplicação web Python.

## Objetivos de Estudo

- **Containerização com Docker**: Aprender a criar imagens Docker para aplicações Python, utilizando Poetry para gerenciamento de dependências.
- **Gerenciamento de Dependências**: Uso do Poetry para definir e instalar dependências de forma isolada.
- **Deploy na Nuvem**: Práticas de implantação contínua em plataformas como Render, utilizando Docker containers.
- **Boas Práticas**: Estruturação de projetos Python, configuração de ambientes virtuais e exposição de portas em containers.

## Tecnologias Utilizadas

- **Python 3.12**: Linguagem de programação principal.
- **Streamlit**: Framework para criação de aplicações web interativas.
- **Poetry**: Ferramenta de gerenciamento de dependências e empacotamento Python.
- **Docker**: Plataforma de containerização para empacotar e executar aplicações.
- **Render**: Plataforma de hospedagem para deploy de aplicações web.

## Estrutura do Projeto

```
aula-docker/
├── app.py              # Código principal da aplicação Streamlit
├── Dockerfile          # Arquivo de configuração para construção da imagem Docker
├── pyproject.toml      # Arquivo de configuração do Poetry com dependências
├── README.md           # Este arquivo
└── __init__.py         # Arquivo de inicialização do pacote Python
```

## Como Executar Localmente

### Pré-requisitos

- Docker instalado na máquina.
- Git para clonar o repositório.

### Passos

1. **Clone o repositório**:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd aula-docker
   ```

2. **Construa a imagem Docker**:
   ```bash
   docker build -t aula-docker .
   ```

3. **Execute o container**:
   ```bash
   docker run -p 8501:8501 aula-docker
   ```

4. **Acesse a aplicação**:
   Abra o navegador e vá para `http://localhost:8501`.

## Deploy no Render

Este projeto está configurado para deploy automático no Render. O Render suporta aplicações containerizadas via Docker, facilitando o processo de implantação.

### Configuração no Render

1. Conecte seu repositório GitHub ao Render.
2. Crie um novo serviço web no Render.
3. Selecione "Docker" como método de build.
4. Configure a porta (8501) e outras opções conforme necessário.
5. Implante a aplicação.

O Render irá automaticamente construir a imagem Docker e executar o container na nuvem.

## Link do Deploy

A aplicação está disponível em: [https://aula-docker-mvnp.onrender.com/](https://aula-docker-mvnp.onrender.com/)

## Contribuição

Este é um projeto de estudo. Sinta-se à vontade para fazer fork, experimentar e contribuir com melhorias!

## Licença

Este projeto é distribuído sob a licença MIT.