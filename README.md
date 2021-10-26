# swift-vapor-dev
Dev Enviroment com o ambiente Swift e Vapor já instalados.

# Como instalar
É possível rodar o devcontainer de dentro de um volume docker ou direto de um diretório Windows.

## Opção A: Devcontainer dentro de volume docker.
1. Faça um fork ou crie um novo repositório utilizando esse de base
2. Iniciar o docker desktop
3. No VS Code:
   - Instalar a extensão Remote - Containers
`ctrl + shift + p` > _Repository in Container Volume_
   - Colar o endereço do fork de https://github.com/medvish1/swift-vapor-dev
   - Abrir o terminal do vs code e executar `sh ./run.sh`. 
     - _Isso irá instalar tds as dependências e iniciar o servidor na porta 8080_

> **AVISO**: Seus fontes estarão dentro de um volume docker, __e não em um diretório no Windows!__. Você deve comitar as alterações para ter acesso aos fontes fora do container
> 
> É possível montar um diretório windows para dentro do dev container (Opção B, listada abaixo), porem as operações como build se tornam bem mais lentas.

## Opção B: Devcontainer em diretório Windows
1. Iniciar o docker desktop
2. Baixar/clonar esse repositorio em uma diretório no seu Windows
3. Abrir a pasta pelo vscode
4. `ctrl + shift + p` > _Reopen in Container_
4. Ao abrir a pasta o code irá sugerir _Reabrir em um devcontainer_.
5. Abrir o terminal do vs code e executar `sh ./run.sh`. 
   - _Isso irá instalar tds as dependências e iniciar o servidor na porta 8080_

> Esse método manterá os fontes dentro do seu Windows.
>
> Porem existe um algo custo em performance. Para mais informações:
> https://code.visualstudio.com/remote/advancedcontainers/improve-performance#_use-clone-repository-in-container-volume


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

