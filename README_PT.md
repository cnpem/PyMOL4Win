# PyMOL de Código Aberto para Windows

O PyMOL de código aberto está disponível gratuitamente. Uma versão pré-compilada de código aberto do PyMOL está disponível gratuitamente em [Christoph Gohlke](https://www.cgohlke.com/) do Departamento de Engenharia Biomédica, Universidade da Califórnia, Irvine.

Este repositório fornece um método para instalar o PyMOL v3.2 no Windows. Se necessário, uma versão em inglês deste guia está disponível [aqui](https://github.com/cnpem/PyMOL4Win/blob/main/README.md).

## Download e Instalação

Siga estes passos para instalar o PyMOL v3.2:

1. Instale a versão mais recente do Python (v3.13.x) para Windows a partir [aqui](http://www.python.org/downloads/).

_Observação_: Certifique-se de que a opção para adicionar variáveis de ambiente esteja selecionada ou adicione a pasta do python.exe ao PATH do sistema.

2. Instale os pacotes Python necessários

```cmd
python -m pip install numpy
python -m pip install pmw
python -m pip install pyqt5
```

3. Baixe arquivos "wheel" de PyMOL de código aberto pré-compilados, compatíveis com Python 3.13 e Windows 64-bit, pelos links abaixo:

* [pymol-launcher](https://github.com/cnpem/PyMOL4Win/releases/latest/download/pymol_launcher-3.2.0a0-cp313-cp313-win_amd64.whl)
* [pymol](https://github.com/cnpem/PyMOL4Win/releases/latest/download/pymol-3.2.0a0-cp313-cp313-win_amd64.whl)

*Observação* : Você pode verificar a versão do Python no anaconda digitando `python --version`.

Se você estiver usando uma versão diferente do Python ou Windows 32-bits, existem outras versões pré-compiladas [aqui](https://github.com/cgohlke/pymol-open-source-wheels/releases).

A estrutura do nome do arquivo é a seguinte:

```cmd
pymol‑3.2.0a0‑cp313‑cp313‑win_amd64.whl
         \         \          \
          \         \          \___ para 64 bits do Windows
           \         \
            \         \____________ para Python 3.13.x
             \
              \____________________ versão PyMOL 3.2.0a0
```

4. Instale os arquivos "wheel":

No Prompt de Comando (não no PowerShell!), navegue até a pasta onde os arquivos foram baixados (por exemplo, `C:\Usuários\<Seu Nome de Usuário>\Downloads`):

```cmd
cd Downloads
```

Em seguida, instale o `pymol_launcher-3.2.0a0-cp313-cp313-win_amd64.whl` digitando:

```cmd
python -m pip install --no-index --find-links="%CD%" pymol_launcher-3.2.0a0-cp313-cp313-win_amd64.whl
```

Depois, instale o `pymol-3.2.0a0-cp313-cp313-win_amd64.whl` com:

```cmd
python -m pip install --upgrade --no-deps pymol-3.2.0a0-cp313-cp313-win_amd64.whl
```

> **Observação:** Se você baixou arquivos diferentes no Passo 3, substitua

*Observação*: Se você baixou arquivos diferentes no Passo 4, substitua `pymol_launcher-3.2.0cp313-cp313-win_amd64.whl` e `pymol-3.2.0a0-cp313-cp313-win_amd64.whl` pelos arquivos wheel baixados.

5. Inicie o PyMOL v3.2

No prompt de comando (não no PowerShell!), execute:

```cmd
where.exe pymol
pymol
```

Então, o PyMOL v3.2 será iniciado e pronto para uso.

6. (Opcional) Criar um atalho para o PyMOL

```cmd
where.exe pymol
```

A localização do `PyMOL.exe` será exibida. Vá até a localização do arquivo, clique com o botão direito em `PyMOL.exe` e copie-o para sua Área de Trabalho.
