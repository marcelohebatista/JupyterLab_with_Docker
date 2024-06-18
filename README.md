### Explicação do Comando

- **`docker run`**: Comando básico do Docker para criar e iniciar um novo contêiner.
- **`-u root`**: Executa o contêiner como usuário root.
- **`--rm`**: Remove automaticamente o contêiner quando ele é encerrado.
- **`-e GRANT_SUDO=yes`**: Define a variável de ambiente `GRANT_SUDO` como "yes".
- **`-e NB_GID=100`**: Define a variável de ambiente `NB_GID` como "100".
- **`-p 8888:8888`**: Mapeia a porta 8888 do contêiner para a porta 8888 no host.
- **`-e JUPYTER_ENABLE_LAB=yes`**: Habilita a interface do JupyterLab por padrão.
- **`-v "$PWD":/home/jovyan/work`**: Monta o diretório de trabalho atual do host em `/home/jovyan/work` dentro do contêiner.
- **`jupyter/datascience-notebook`**: Especifica a imagem Docker a ser usada.
- **`start-notebook.sh`**: Comando para iniciar o servidor Jupyter Notebook.
- **`--NotebookApp.token='python'`**: Define o token inicial para o servidor Jupyter Notebook.

## Execução do Comando Docker

Para executar o comando Docker, abra um terminal e digite o seguinte comando:

```bash
docker run -u root --rm -e GRANT_SUDO=yes -e NB_GID=100 -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v "$PWD":/home/jovyan/work jupyter/datascience-notebook start-notebook.sh --NotebookApp.token='python'
```

Este comando iniciará um contêiner Docker com a imagem `jupyter/datascience-notebook` e configurará o JupyterLab conforme descrito anteriormente.

## Acessando o JupyterLab

Após executar o comando Docker, você verá uma saída no terminal indicando que o servidor JupyterLab foi iniciado. Para acessar o JupyterLab, abra um navegador da web e vá para o seguinte endereço:

```
http://localhost:8888
```

Você será solicitado a inserir um token. Use o token definido no comando Docker, que neste caso é "python".

## Conclusão

Neste guia, exploramos como executar um contêiner Docker usando a imagem `jupyter/datascience-notebook` e como acessar o JupyterLab. Este comando é uma ferramenta poderosa para cientistas de dados que desejam rapidamente configurar um ambiente de desenvolvimento com todas as ferramentas e bibliotecas necessárias.

Esperamos que este guia tenha sido útil e que você aproveite ao máximo o JupyterLab para suas análises de dados!

## Referências

- [Docker Hub: jupyter/datascience-notebook](https://hub.docker.com/r/jupyter/datascience-notebook)
- [Site Oficial do Docker](https://www.docker.com/get-started)
```
