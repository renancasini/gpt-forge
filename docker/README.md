# Docker base — gpt-forge

Este diretório contém imagens base reutilizáveis.

## Objetivo
- Centralizar padrões Docker
- Evitar duplicação entre projetos
- Servir como base para imagens finais

## Uso típico em projetos
```dockerfile
FROM gpt-forge/base:latest
