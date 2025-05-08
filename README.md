# Deploy-AWS-EC2-Projeto-Mundo-Invertido
🌐 Deploy AWS EC2 — Projeto Mundo Invertido Seu primeiro deploy gratuito e funcional na AWS com Run as Cloud

## 🧾 1. Criar uma instância EC2 (Free Tier)

- **AMI:** Amazon Linux 2023  
- **Nome da instância:** `EC2 - Mundo Invertido`  
- **Tipo de instância:** `t2.micro` (Free Tier)  
- **Par de chaves:** `EC2-Tutorial.pem` *(salve no seu computador!)*  
- **Grupo de Segurança:**
  - Porta `22 (SSH)` – acesso remoto  
  - Porta `80 (HTTP)` – visualizar o site

## ⚠️ **Importante:** Após terminar o projeto, **delete a instância** para evitar custos!

---

## 📥 2. Acessar a instância

### ✅ Método 1 — EC2 Instance Connect (via navegador)

1. Vá no Console AWS > EC2  
2. Selecione a instância `EC2 - Mundo Invertido`  
3. Clique em **"Connect"**  
4. Vá na aba **"EC2 Instance Connect"**  
5. Clique em **"Connect"**

### ✅ Método 2 — SSH via Git Bash (com `.pem`)

```bash
cd ~/Downloads
chmod 400 EC2-Tutorial.pem
ssh -i "EC2-Tutorial.pem" ec2-user@<IP_DNS_Público>
````

![image](https://github.com/user-attachments/assets/29c62776-1b70-4dea-bb04-556e658003f5)

![image](https://github.com/user-attachments/assets/59c9dc43-69fe-47ce-9905-357842c053cd)

![image](https://github.com/user-attachments/assets/fafe8e8c-1f69-4455-b4af-2210b0c56f28)

![image (96)](https://github.com/user-attachments/assets/7fbe0e8f-197b-40cd-9641-833bd1cc7dff)

![image](https://github.com/user-attachments/assets/5eb89855-994b-45fa-adfb-fbb0643e219d)

### ⚙️ 3. Instalar Apache, Git e clonar o projeto

### Atualizar pacotes
```bash
sudo yum update -y
````

### Instalar Apache
```bash
sudo yum install httpd -y
````

### Iniciar e habilitar Apache
```bash
sudo systemctl start httpd
sudo systemctl enable httpd
````

### Instalar Git
```bash
sudo yum install git -y
````

### Clonar o projeto
```bash
git clone https://github.com/HebertonGeovane/mundo-invertido.git
````

### 📂 4. Copiar arquivos para o Apache

### Copiar arquivos do projeto para o diretório do Apache
```bash
sudo cp -r ~/mundo-invertido/* /var/www/html/
````

### Ajustar permissões
```bash
sudo chmod -R 755 /var/www/html
````

![image](https://github.com/user-attachments/assets/8db3cf57-6c8a-4594-a49e-d72e438d1849)

![image](https://github.com/user-attachments/assets/969b6302-2d2d-4652-bcd7-9f911185948d)

![image](https://github.com/user-attachments/assets/db643ef6-4c83-414e-83b6-db14db50302f)


### 🌍 5. Acessar o site

### Abra no navegador:
```bash
http://<SEU_IP_PUBLICO>
````
### 🎉 Pronto! Seu site Mundo Invertido está online!

![image](https://github.com/user-attachments/assets/52e8b3cb-031a-43de-9c2f-f0fe49946a4f)

![image](https://github.com/user-attachments/assets/485de8d6-fbc9-4753-b3e8-379b5b133fe1)

## 🚨 Lembrete Final
## ⚠️ Importante: Após terminar o projeto, delete a instância para evitar custos!

### 📸 Prints do Processo
Instância EC2 criada

Acesso via navegador ou terminal

Instalação do Apache e Git

Site funcionando

## 🤝 Compartilhe seu progresso!
Marque:

A comunidade Run as Cloud  https://www.linkedin.com/company/run-as-cloud/?viewAsMember=true

Os ADMs dos Grupos de Estudos https://www.linkedin.com/in/maik-biazi-47b9291a5/  |   https://www.linkedin.com/in/mernesto/

E me marque também 😄  https://www.linkedin.com/in/heberton-geovane/




