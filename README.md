# swift-vapor-dev

Dev Enviroment com o ambiente Swift e Vapor já instalados.

Contem o projeto hello world do vapor.

## Obtendo o devcontainer

### Clonando o repositório e um volume docker
Essa é a forma mais recomentada.

Faça o fork ou um novo repositório utilizando esse como base.

Aperte ctrl + p e selecione _clone Repository in Container Volume_ e cole o caminho do repositorio

VS Code irá baixar o repositorio e iniciar o dev container.

Docs: https://code.visualstudio.com/remote/advancedcontainers/improve-performance#_use-clone-repository-in-container-volume 

### Diretório no Windows
É possível simplesmente baixar/clonar esse repositorio em uma diretório no seu windows e acessa-lo pelo vscode.
Ao abrir a pasta o code irá sugerir _Reabrir em um devcontainer_.
Clique no botão e aguarde o container ser iniciado.

> Existe uma grande penalidade em performance utilizando este método


## Rodando
Para iniciar o servidor execute o  `run.sh`, ou rode o comando
```bash
vapor run serve -b 0.0.0.0:8080
```
_[Documentação run](https://docs.vapor.codes/4.0/server/#serve-command)_

> A primeira execução pode levar **vários minutos**, para clonar e compilar todas as dependencias.


## Extensões

Caso as extenções não sejam automaticamente instaladas:
Instale as mesmas no container:
- [SourceKit-LSP - Unofficial CI build](https://marketplace.visualstudio.com/items?itemName=pvasek.sourcekit-lsp--dev-unofficial)
- [Maintained Swift Development Environment](https://marketplace.visualstudio.com/items?itemName=vknabel.vscode-swift-development-environment)
- [CodeLLDB](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb)

> É necessário reiniciar o VS Code após instalar as etenções

## Avisos
Não é possível iniciar o servidor equnato o plugin estiver fazendo o build.

