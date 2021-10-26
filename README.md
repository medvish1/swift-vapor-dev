# swift-vapor-dev
Dev Enviroment com o ambiente Swift e Vapor já instalados.

## Obtendo o devcontainer
1. Faça um fork ou crie um novo repositório utilizando esse de base
2. Iniciar o docker desktop
3. No VS Code:
   - Instalar a extensão Remote - Containers
ctrl + shift + p > Repository in Container Volume
   - Colar o endereço do fork de https://github.com/medvish1/swift-vapor-dev
   - Abrir o terminal do vs code e executar `sh ./run.sh`. 
     - _Isso irá instalar tds as dependências e iniciar o servidor na porta 8080_


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
