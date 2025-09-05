# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas linguagens Python, JavaScript, TypeScript e Java, e gera relatórios `HTML` como [este](https://andrehora.github.io/gitevo-examples/python/pandas.html).

Mais exemplos de relatórios podem ser podem ser encontrados em https://github.com/andrehora/gitevo-examples.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

> [!NOTE]
> Antes de instalar a ferramenta, é recomendado criar e ativar um [ambiente virtual Python](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#create-and-use-virtual-environments).

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
$ pip install gitevo
```

Execute a ferramenta no repositório selecionado utilizando o comando abaixo (ajuste conforme a linguagem do repositório).
Substitua `<git_url>` pela URL do repositório que será analisado:

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r javascript <git_url>

# TypeScript
$ gitevo -r typescript <git_url>

# Java
$ gitevo -r java <git_url>
```

Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

> [!NOTE]
> Essa etapa pode demorar alguns minutos pois o projeto será clonado e analisado localmente.

# Passo 3: Explorar o relatório de evolução de código

Após executar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), é gerado um relatório `HTML` contendo diversos gráficos sobre a evolução do código.

Abra o relatório `HTML` e observe com atenção os gráficos.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo
- Detalhar se as curvas estão de acordo com boas práticas
- Explicar grandes alterações nas curvas
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- etc.

Seja criativo!

# Instruções para o exercício

1. Crie um `fork` deste repositório (mais informações sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Adicione o relatório `HTML` no seu fork.
3. No Moodle, submeta apenas a URL do seu `fork`.

Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork:

**1. Repositório selecionado:** https://github.com/SeleniumHQ/selenium.git

**2. Gráfico selecionado:** 

<img width="834" height="404" alt="image" src="https://github.com/user-attachments/assets/ff9de83b-e508-443e-be6c-b6673dbaa292" />


**3. Explicação:** O Selenium é uma ferramenta desenvolvida majoritariamente em Java, e é usada para a automação de testes de aplicações web. Seu código como um todo possui pouco mais de 170 mil linhas de código registradas em 2025. Dessas linhas, algumas são comentários, como pode ser observado no gráfico acima. É possível notar pela imagem que a quantidade de comentários em linha caiu de 25932 (2020) para 22190 (2025), enquanto que a quantia de comentários em bloco manteve-se quase estável, com uma pequena diferença de 1555 (2020) para 1368 (2025). Essa queda, principalmente referente aos comentários em linha, pode indicar que houve uma refatoração no código do Selenium, visto que os comentários não fossem mais necessários após deixar o código mais autoexplicativo, com nomes de variáveis, funções e classes de claro entendimento. Além disso, devido à estabilidade, pode-se concluir que os desenvolvedores se preocuparam em não lotar o programa com comentários desnecessários, usando apenas aqueles que fossem precisos. Portanto, as curvas demonstram que boas práticas foram aplicadas no desenvolvimento da ferramenta, e que a busca por um código mais limpo está sendo realizada por seus desenvolvedores.



