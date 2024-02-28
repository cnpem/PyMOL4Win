# PyMOL de Código Aberto para Windows

O PyMOL de código aberto está disponível gratuitamente. Uma versão pré-compilada de código aberto do PyMOL está disponível gratuitamente em [Christoph Gohlke](https://www.cgohlke.com/) do Departamento de Engenharia Biomédica, Universidade da Califórnia, Irvine.

Este repositório fornece um método para instalar o PyMOL v2.6 no Windows. Se necessário, uma versão em inglês deste guia está disponível [aqui](https://github.com/LBC-LNBio/PyMOL4Win/blob/main/README.md).

## Download e Instalação

Siga estes passos para instalar o PyMOL v2.6:

1. Instale a versão mais recente do Python (v3.12.x) para Windows a partir [aqui](http://www.python.org/downloads/).

_NOTE_: Certifique-se de que a opção para adicionar variáveis de ambiente esteja selecionada ou adicione a pasta do python.exe ao PATH do sistema.

2. Instale os pacotes Python necessários

```cmd
python -m pip install numpy
python -m pip install pmw
python -m pip install pyqt5
```

3. Baixe arquivos "wheel" de PyMOL de código aberto pré-compilados, compatíveis com Python 3.12 e Windows 64-bit, pelos links abaixo:

* [pymol-launcher](https://github.com/LBC-LNBio/PyMOL4Win/releases/latest/download/pymol_launcher-2.5-cp312-cp312-win_amd64.whl)
* [pymol](https://github.com/LBC-LNBio/PyMOL4Win/releases/latest/download/pymol-2.6.0a0-cp312-cp312-win_amd64.whl)

*Observação* : Você pode verificar a versão do Python no anaconda digitando `python --version`.

Se você estiver usando uma versão diferente do Python ou Windows 32-bits, existem outras versões pré-compiladas [aqui](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pymol).

A estrutura do nome do arquivo é a seguinte:

```cmd
pymol‑2.6.0a0‑cp312‑cp312‑win_amd64.whl
         \         \          \
          \         \          \___ para 64 bits do Windows
           \         \
            \         \____________ para Python 3.12.x
             \
              \____________________ versão PyMOL 2.6.0a0
```

4. Instale os arquivos "wheel"

Na janela do CMD (não do PowerShell!), mude para o diretório de download (`C:\Usuários\<Seu Nome de Usuário>\Downloads`):

```cmd
cd Downloads
```

Em seguida, instale `pymol_launcher-2.6-cp312-cp312-win_amd64.whl` digitando:

```cmd
python -m pip install --no-index --find-links="%CD%" pymol_launcher-2.6-cp312-cp312-win_amd64.whl
```

Por fim, para instalar `pymol-2.6.0a0-cp312-cp312-win_amd64.whl`, execute:

```cmd
pip install --upgrade --no-deps pymol-2.6.0a0-cp312-cp312-win_amd64.whl
```

*Observação*: Se você baixou arquivos diferentes no Passo 4, substitua pymol_launcher-2.6-cp312-cp312-win_amd64.whl e pymol-2.6.0a0-cp312-cp312-win_amd64.whl pelos arquivos wheel baixados.

5. Inicie o PyMOL v2.6

No prompt de comando (não no PowerShell!), execute:

```cmd
where.exe pymol
pymol
```

Então, o PyMOL v2.6 será iniciado e pronto para uso.

6. (Opcional) Criar um atalho para o PyMOL

```cmd
where.exe pymol
```

A localização do `PyMOL.exe` será exibida. Vá até a localização do arquivo, clique com o botão direito em `PyMOL.exe` e copie-o para sua Área de Trabalho.
