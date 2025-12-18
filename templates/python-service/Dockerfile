# syntax=docker/dockerfile:1

# Imagem base padronizada do gpt-forge
FROM gpt-forge/base:latest

# Diretório de trabalho
WORKDIR /app

# Variáveis de ambiente padrão
ENV PYTHONUNBUFFERED=1 \
    PYTHONDONTWRITEBYTECODE=1

# Copia apenas requirements primeiro (cache eficiente)
COPY requirements.txt /app/requirements.txt

# Instala dependências do projeto
RUN pip install --no-cache-dir -r requirements.txt

# Copia o restante do código
COPY . /app

# Porta padrão (ajustável por projeto)
EXPOSE 8000

# Comando padrão (sobrescrevível)
CMD ["python", "main.py"]
