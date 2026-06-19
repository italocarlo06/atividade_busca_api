# Atividades de Programação Web - Consumo de APIs

Este repositório contém atividades práticas para o aprendizado de consumo de APIs utilizando JavaScript (Fetch API).

> [!NOTE]
> Como exemplo de referência de um projeto que consome API, vocês podem olhar o repositório [Pokefinder](https://github.com/italocarlo06/pokefinder).

## 🚀 Atividades

### 1. Busca de Times (SportsDB API)
Nesta atividade, você desenvolverá uma aplicação que permite buscar informações sobre times de futebol.

- **URL Base:** `https://www.thesportsdb.com/api/v1/json/123/searchteams.php`
- **Parâmetro:** `t` (nome do time)
- **Exemplo de busca:** `https://www.thesportsdb.com/api/v1/json/123/searchteams.php?t=Flamengo`

#### O que deve ser feito:
- Criar um campo de busca para o usuário digitar o nome do time.
- Realizar a requisição utilizando `fetch` com `async/await`.
- **Atenção:** A API retorna um objeto contendo um array chamado `teams`. Você deve acessar o primeiro item desse array (ex: `data.teams[0]`) para obter os dados do time.
- Exibir as seguintes informações:
  - Escudo do time (`strTeamBadge`)
  - Nome do time (`strTeam`)
  - Nome do Estádio (`strStadium`)
  - Capacidade do Estádio (`intStadiumCapacity`)
  - Cidade (`strLocation`)

---

### 2. Consulta de Clima (WeatherAPI)
Nesta atividade, você criará um painel que mostra as condições climáticas atuais de uma cidade informada.

- **Endpoint:** `https://api.weatherapi.com/v1/current.json`
- **Parâmetros necessários:**
  - `key`: Sua chave de API.
  - `q`: Nome da cidade.
  - `aqi=no`: Desabilita dados de qualidade do ar.
  - `lang=pt`: Retorna as descrições em português.
- **Exemplo de URL:**
  ```javascript
  const apiKey = 'SUA_CHAVE_AQUI';
  const city = 'Maceio';
  const apiUrl = `https://api.weatherapi.com/v1/current.json?key=${apiKey}&q=${city}&aqi=no&lang=pt`;
  ```

#### O que deve ser feito:
- Obter uma chave gratuita em [WeatherAPI](https://www.weatherapi.com/).
- Criar uma interface baseada no `index.html` fornecido.
- Exibir dinamicamente as seguintes informações retornadas pela API:
  - Nome da Cidade (`location.name`)
  - Hora Local (`location.localtime`)
  - Ícone da Condição (`current.condition.icon`)
  - Temperatura Atual (`current.temp_c`)
  - Condição Climática (`current.condition.text`)
  - Sensação Térmica (`current.feelslike_c`)
  - Umidade (`current.humidity`)
  - Velocidade do Vento (`current.wind_kph`)
  - Pressão Atmosférica (`current.pressure_mb`)
  - Visibilidade (`current.vis_km`)
  - Índice UV (`current.uv`)

---

> [!TIP]
> **Diferencial de Customização (Para ambos os projetos):**
> Você pode ir além do básico e exibir informações extras, como o ano de fundação e redes sociais (no caso de times) ou dados climáticos adicionais (no caso de clima). Use sua criatividade no layout para organizar esses dados de forma elegante! Isso será levado em consideração como um diferencial na avaliação.

## 📤 Entrega da Atividade

Para concluir a atividade, siga estes passos:

1. **Crie um repositório no GitHub** com o nome do tema escolhido (ex: `atividade-clima` ou `busca-times`).
2. **Suba seus arquivos** (`index.html`, `style.css`, `script.js`) para este repositório.
3. **Publique no GitHub Pages**:
   - Vá em *Settings* > *Pages*.
   - Em *Branch*, selecione `main` e clique em *Save*.
4. **Envie o link** do seu repositório e o link do site publicado conforme as orientações do professor.

---

## 🛠️ Como realizar as atividades

1. Crie uma função `async` para realizar a busca.
2. Utilize o comando `await fetch(url)` para buscar os dados.
3. Converta a resposta para JSON: `const data = await response.json()`.
4. Manipule o DOM para exibir os dados na tela.
5. Utilize um bloco `try/catch` para tratar possíveis erros.

### Exemplo de estrutura:
```javascript
async function buscarDados() {
    try {
        const response = await fetch(url);
        const data = await response.json();
        console.log(data);
    } catch (error) {
        console.error('Erro ao buscar dados:', error);
    }
}
```

Bons estudos! 🚀
