# Introdução ao Git e Deploy automático no servidor
Instale o Git o git para Linux: https://book.git-scm.com/download/linux

Tutorial em: https://youtu.be/9QRauzuaX2M

Salientando que todos os comandos git podem ser realizadas de forma interativa no próprio Github, como alterações nos arquivos e um pull request com uma sugestão de outro usuário.


Entre no github, crie um novo repositório, entre numa pasta no pc e siga as instruções (indicadas pelo github):

# Create a new repository on the command line:
- echo "# oi" >> README.md      # insere oi no README
- git init  		      # É criado uma pasta oculto .git com arquivos de controle e pastas ocultas
- git add . 		      # adiciona todos os arquivos e atualizações à pasta index (intermedária)
- git commit -m "first commit"  #repassa os arquivos para a pasta HEAD com commit
- git remote add origin https://github.com/SanUSB/oi.git  #endereça o repositório remoto
- git push -u origin master     #posta os arquivos na branch (ramo ou filial) master

Para resgatar a última versão do repositório:

- git clone https://github.com/SanUSB/oi.git <nome da pasta no pc>

 ou 

- git init

- git pull https://github.com/SanUSB/oi

# Deploy Automático:

Inserir a chave ssh e a URL Webhook no projeto do Github (private, funcionou public) -> em settings -> Webhooks.

Todo o conteúdo que for enviado via push no github será atualizado na página do servidor, por exemplo, hostinger.

Testado e funciona somente quando o repositório é public (settings -> public).
