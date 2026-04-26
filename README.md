# Laboratorio-de-Industria-Fisico-Quimico-de-Extracao-de-oleo-de-Soja
Atividade pratica para a Disciplina AI Factory: Building  Intelligents Systens 
# Projeto

Este projeto agora possui uma stack Docker com:

- `streamlit-chat` em `http://localhost:8501`
- `flowise` opcional em `http://localhost:3000`

## Como usar

1. Ajuste o arquivo `streamlit-chat/.env` com o `FLOWISE_API_URL` e o `FLOWISE_BEARER_TOKEN`
2. Na raiz do projeto, rode:

```bash
docker compose up --build
```

Se o container do Streamlit ja estiver criado e voce trocar dependencias, rode novamente com `--build` para recriar a imagem.

Se quiser que esta stack tambem suba um container novo do Flowise:

```bash
docker compose --profile flowise up --build
```

## Estrutura

- `Flowise/`: codigo-fonte do Flowise
- `streamlit-chat/`: app Streamlit com interface de chat
- `docker-compose.yml`: sobe os dois containers juntos
