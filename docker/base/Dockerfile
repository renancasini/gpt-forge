# syntax=docker/dockerfile:1

FROM python:3.12-slim

# Variáveis padrão
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Dependências do sistema (mínimas e comuns)
RUN apt-get update && apt-get install -y \
    build-essential \
    curl \
    git \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

# Diretório padrão de trabalho
WORKDIR /app

# Usuário não-root (boa prática)
RUN useradd -m appuser
USER appuser
