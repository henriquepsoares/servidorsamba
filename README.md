📂 Projeto: Servidor de Arquivos com Samba

Este é um projeto que eu, Henrique Soares, configurei para criar um servidor de arquivos em rede usando Samba no Debian. O objetivo foi criar uma solução de compartilhamento de arquivos acessível a todas as máquinas da rede.

🖥️ Sobre o Projeto
Criei a pasta compartilhada trabalho
Configuração do Samba para permitir acesso sem senha
Testado em máquinas Linux e Windows na rede interna
Ideal para pequenas redes ou ambientes de laboratório

⚙️ Passo a Passo da Configuração

Instalar Samba:

sudo apt update
sudo apt install samba

Criar a pasta compartilhada:
sudo mkdir -p /srv/samba/trabalho
sudo chmod 777 /srv/samba/trabalho

Configurar Samba:
[trabalho]
   path = /srv/samba/trabalho
   browseable = yes
   read only = no
   guest ok = yes

Reiniciar Samba:

sudo systemctl restart smbd
sudo systemctl enable smbd

Acessar a pasta da rede:

Linux: smb://IP_DO_SERVIDOR/trabalho
Windows: \\IP_DO_SERVIDOR\trabalho

📷 Capturas de Tela do Projeto


Servidor mostrando a pasta trabalho


Pastas acessíveis pelas máquinas da rede

👤 Sobre o Autor

Henrique Soares (He/Him)

💻 Senior Cloud Security & DevOps Engineer
☁️ Azure, AWS
🔧 Terraform • CI/CD • Kubernetes
🚀 Infrastructure as Code (IaC)
🌐 Networking & Cybersecurity
📡 Cisco Meraki
📍 Edinburgh / London