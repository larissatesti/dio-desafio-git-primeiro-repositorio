# Introdução ao Git e ao GitHub



* O que é Git: Versionamento de código distribuído.



## Benefícios de aprender Git e GitHub juntos:

1) Controle de versão
2) Armazenamento em nuvem
3) Trabalho em Equipe
4) Melhorar código
5) Reconhecimento



## Diferenças no Windows e Linux (comandos):

**Listar**: Windows = dir
			Linux = ls

**Navegar entre pastas**: cd /

**Retroceder**: cd ..

**Limpar a tela**: Windows = cls
							Linux = clear (ou CTRL + L)

**Criar pasta**: mkdir *nome da pasta*

**Para deletar arquivos**:  del

**Para deletar repositório**: Windows = rmdir workspace /s /q
												Linux = rm - rf

| Windows   | Unix   | Obs    |
| --------- | ------ | ------ |
| cd        | cd     | muda   |
| dir       | ls     | lista  |
| mdkir     | mkdir  | cria   |
| del/rmdir | rm -rf | deleta |



# Git por baixo dos panos

**SHA** - Secure Hash Algorithm é um conjunto de funções hash criptográficas projetadas pela NSA. A encriptação gera um conjunto de characteres identificados de 40 dígitos (únicos).

* SHA1:
  * Objetos fundamentais
  * Sistema distribuído
  * Segurança 

### Objetos internos do GIT

* BLOBS (não guarda nome)
* TREES:
  * Armazenam blobs
  * Apontam blob ou outras árvores
  * Tem SHA1 desse metadado
* COMMITS
  * Objeto que junta tudo
  * Aponta para árvore,parente, autor, mensagem, timestamp
  * o SHA1 desse commit é o hash de toda essa informação

## Chave SSH e Token 

**Chave SSH**  - forma segura e máquina confiável

* Imagem > settings > SSH > new SSH Key

**Token** 

* Developer settings > personal access tokens.



## Comandos Git

* git init (inicializa um repositório git na pasta em questão)
* git add
* git commit

_ls - a_ mostra ass páginas ocultas

_git add *_  todas as modificações

_git commit -M "commit inicial"_



## Ciclo de vida dos arquivos no Git

- Unmodified
- Modified
- Staged

Servidor - remote repository

| Ambiente de desenv. | Working directory | Staging area | Local repository |
| ------------------- | ----------------- | ------------ | ---------------- |

_git status_ verifica status

_mv_ mover, exemplo:

					- _mkdir receitas_ (criei)
					- _ls_ (listei)
					- _mv novareceita.md ./ receitas /_

## GitHub

git config -- list

git config -- global == unset user._email_

git config -- global -- unset user._name_ 



**Para colocar emai e nickname**:

git config -- global user.email seuemail@email

git config -- global user.name _nome_ 



**Repositórios** 

1. Criar um repositório no github
2. Copiar o link do repositório
3. git remote add origin https.... get (para verificar se criou utilizar _git remote -v_)
4. git push origin master



**Resolvendo conflitos**:

git pull origin master (puxar o que está no github para a máquina)



**Criando o 1º repositório**: 

1. Criar um repositório
2. Para clonar: _git clone https...._
3. Para entrar na pasta: _cd nomedapasta_
4. Alterar localmente as alterações feitas na máquina: _git add ._
5. Para passar ao GitHub: _git commit -M "inclusão das anotações, ex"_
6. Para finalizar: _git push origin main_



