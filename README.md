# Docker

## Guia de Instalação Docker
Este guia ajuda a configurar o ambiente Docker necessário para executar este projeto. 
## Pré-requisitos
Windows: Windows 10/11 com WSL2 habilitado.
macOS: Chip Intel ou Apple Silicon (M1/M2/M3).
Linux: Distribuição 64 bits (Ubuntu, Debian, CentOS, etc.). 
## 1. Instalação (Windows e macOS)
A maneira mais fácil é instalar o Docker Desktop. 
Baixe o instalador: Docker Desktop
Execute o arquivo baixado e siga o assistente de instalação.
Windows: Certifique-se de marcar a opção "Use WSL 2 instead of Hyper-V" durante a instalação.
Inicie o Docker Desktop após a instalação. 
YouTube
YouTube
 +3
## 2. Instalação (Linux - Ubuntu/Debian)
Execute os comandos no seu terminal para instalar o Docker Engine: 
bash
# Atualize o índice de pacotes
sudo apt-get update

# Instale os pacotes necessários
sudo apt-get install ca-certificates curl gnupg lsb-release

# Adicione a chave GPG oficial do Docker
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://docker.com | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

# Configurar o repositório
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://docker.com \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Instale o Docker Engine
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
## Rodar Docker sem sudo (Opcional - Recomendado) 
Para evitar digitar sudo em todos os comandos docker:
bash
sudo usermod -aG docker $USER
# Reinicie o computador ou faça logout/login
## 3. Verificação
Abra o terminal (ou PowerShell) e execute: 
bash
docker --version
docker run hello-world
Se a mensagem "Hello from Docker!" aparecer, a instalação foi bem-sucedida. 
YouTube
YouTube
 +2
🚀 Como rodar o projeto
Após clonar o repositório, execute na pasta do projeto: 
bash
docker compose up --build
