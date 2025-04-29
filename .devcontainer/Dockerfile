# Dockerfile para Codespaces / DevContainer
FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

# Instala dependências básicas
RUN apt-get update && \
    apt-get install -y curl && \
    rm -rf /var/lib/apt/lists/*

# Executa o script de instalação do Phlow
RUN curl -fsSL https://raw.githubusercontent.com/phlowdotdev/phlow/main/scripts/install-phlow.sh | bash || true

# (opcional) Garante que ~/.bashrc tenha o PATH do Phlow
RUN echo 'export PATH="$HOME/.phlow:$PATH"' >> /root/.bashrc
