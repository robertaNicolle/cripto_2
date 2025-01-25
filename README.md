# Cripto_2 - Consulta de Cotação de Criptomoedas

Este projeto em Python permite consultar a cotação de criptomoedas em relação a diferentes moedas fiduciárias usando a API **CoinGecko**. A interface gráfica é construída com o Tkinter, permitindo ao usuário interagir facilmente e obter as informações em tempo real.

## Funcionalidades

- **Consulta de Cotação de Criptomoedas**: O sistema permite que o usuário busque a cotação de uma criptomoeda em relação a moedas como BRL, USD, entre outras.
- **Interface Gráfica (GUI)**: A aplicação conta com uma interface gráfica simples e intuitiva, desenvolvida com o Tkinter, onde o usuário insere o nome da criptomoeda e a moeda de referência para consulta.
- **Feedback de Carregamento**: Exibe uma mensagem de "Carregando..." enquanto a consulta está sendo feita para melhorar a experiência do usuário.
- **Resultados Formatados**: Exibe o resultado da cotação de forma clara e bem formatada, com tratamento de erros caso algo dê errado.

## Estrutura do Projeto

- `api.py`: Contém a função `obter_cotacao_cripto` responsável por fazer a requisição à API CoinGecko para obter a cotação da criptomoeda.
- `main.py`: Arquivo principal que contém a implementação da interface gráfica com Tkinter. Também é responsável por interagir com o usuário e exibir as cotações.
  
## Como Rodar o Projeto

### Requisitos
- Python 3.x
- Bibliotecas: `requests`, `tkinter` (incluída no Python por padrão)

### Passo a Passo

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/cripto_2.git
   ```

2. Navegue até o diretório do projeto:
   ```bash
   cd cripto_2
   ```

3. Instale as dependências:
   ```bash
   pip install requests
   ```

4. Execute a aplicação:
   ```bash
   python main.py
   ```

### Como Usar

1. Abra o aplicativo e insira o nome da criptomoeda (exemplo: `bitcoin`).
2. Insira a moeda de referência (exemplo: `usd`, `brl`).
3. Clique em **Buscar Cotação** e aguarde a exibição do valor da criptomoeda.
4. Caso precise, clique em **Limpar** para reiniciar os campos de entrada.
5. Para sair do aplicativo, clique em **Sair** e confirme a ação.

## Demonstração da Interface

### Tela Inicial:
A interface gráfica inicial exibe campos para o nome da criptomoeda e da moeda de referência.

### Resultados:
Após a consulta, o valor da criptomoeda será exibido de forma clara, com o preço formatado, e se houver algum erro, será mostrada uma mensagem indicando o tipo de erro.

## Como Funciona

1. O usuário insere a **criptomoeda** (exemplo: `bitcoin`) e a **moeda de referência** (exemplo: `brl`).
2. A função `obter_cotacao_cripto` faz uma requisição HTTP à API **CoinGecko** para obter a cotação atual da criptomoeda em relação à moeda informada.
3. A cotação é exibida na interface gráfica.
4. Caso ocorra algum erro (como um erro de conexão ou criptomoeda inválida), uma mensagem de erro será apresentada ao usuário.

## Exemplo de Saída

Se o usuário consultar a cotação do **Bitcoin** (BTC) em relação ao **BRL**, o resultado será mostrado assim:

```
A cotação para a BTC em BRL é: 250,000.00
```

Caso ocorra um erro, será exibido algo como:

```
Erro na consulta. Código de erro: Erro na conexão: ...
```

## Tratamento de Erros

- **Erro de conexão**: Se a API CoinGecko não estiver acessível ou houver algum problema de rede, o sistema exibirá uma mensagem informando o erro.
- **Criptomoeda não encontrada**: Se a criptomoeda não for válida ou não estiver registrada na API CoinGecko, o sistema informará que a criptomoeda não foi encontrada.

## Contribuindo

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/cripto_2.git
   ```

2. **Crie um branch**:
   ```bash
   git checkout -b minha-implementacao
   ```

3. **Faça suas modificações** e **commite**:
   ```bash
   git commit -am "Descrição das modificações"
   ```

4. **Envie seu branch**:
   ```bash
   git push origin minha-implementacao
   ```

5. **Abra um Pull Request** para revisão.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---
