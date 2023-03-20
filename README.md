O Stable Diffusion é um software que gera imagens através de inteligência artificial alimentada por um banco de imagens sistematicamente descritas utilizadas como referência na produção de novas imagens. A ferramenta é capaz de produzir imagens com diversos estilos. Em alguns casos, as imagens podem até parecer uma fotografia de tão real ou até mesmo obras de artes famosas. 

A ferramenta foi fundada pela stability.ai em parceria com Runway, desenvolvidos em Python e Jupyter Notebook. Seu primeiro lançamento aconteceu no dia 31 de agosto de 2022. 

[Stability.ai](https://stability.ai/blog/stable-diffusion-public-release)

[huggingface](https://huggingface.co/spaces/stabilityai/stable-diffusion)


# Guia mestre:

[GUIA COMPLETO - INGLÊS](https://rentry.org/voldy) - guia que segui para conseguir utilizar o stable diffusion.

# Máquina utilizada:

* 2x RAM DDR4, 8GB 3000MHz
* AMD Ryzen 5 PRO 4650G
* MOTHERBOARD B450M DS3H V2
* AMD Radeon™ RX 6650 XT 8GB

# Passos:

#### **Passo 1:** [Instalar o GIT](https://git-scm.com/)
-Ao instalar, certifique-se de marcar a caixa para 'integração do Windows Explorer -> Git Bash'

#### **Passo 2:** Clone o repositório WebUI para o local desejado:

```
git clone https://github.com/lshqqytiger/stable-diffusion-webui-directml && cd stable-diffusion-webui-directml && git submodule init && git submodule update
```
#### **Passo 3:** Baixe seu(s) modelo(s) preferido(s):

* [SD 1.5](https://huggingface.co/runwayml/stable-diffusion-v1-5/resolve/main/v1-5-pruned.ckpt) - < versão que estou utilizando

* [SD 2.0](https://huggingface.co/stabilityai/stable-diffusion-2)

* [SD 2.1](https://huggingface.co/webui/stable-diffusion-2-1)

* [Mais modelos](https://rentry.org/sdmodels)

**(1.5 produz [resultados muito melhores](https://www.assemblyai.com/blog/stable-diffusion-1-vs-2-what-you-need-to-know/) do que 2.0 e 2.1)**

#### **Passo 4:** Renomeie seu arquivos .ckpt ou .safetensors para "model.ckpt" ou "model.safetensors" e coloque-o na pasta */models/Stable-diffusion*
 * Você pode ter quantos modelos quiser na pasta, "model" é apenas aquele que ele carregará por padrão

#### **Passo 5:** ![Instale o Python 3.10](https://www.python.org/ftp/python/3.10.6/python-3.10.6-amd64.exe)
Certifique-se de escolher "adicionar ao PATH" ao instalar

#### **Passo 6:** Argumentos (Opcional):
 -Edite webui-user.bat
-mude COMMANDLINE_ARGS= para  COMMANDLINE_ARGS= --precision full --no-half --opt-sub-quad-attention --disable-nan-check

#### **Passo 7:** Rode o webui-user.bat:
Abra-o como usuário normal, não como administrador.
Aguarde pacientemente enquanto ele instala as dependências e faz uma primeira execução. Pode parecer "parado", mas não está. Pode levar de 10 a 15 minutos.
E pronto!

```
Iniciar webui-user.bat
Depois de carregar o modelo, ele deve fornecer um endereço LAN como '127.0.0.1:7860'
Digite o endereço em seu navegador para entrar no ambiente GUI
Dica: passe o mouse sobre os elementos da interface do usuário para obter dicas sobre o que eles fazem
Para sair, feche a janela CMD
```
