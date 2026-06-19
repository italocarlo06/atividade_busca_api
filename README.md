# Atividades de Programação Web - Consumo de APIs

Este repositório contém atividades práticas para o aprendizado de consumo de APIs utilizando JavaScript (Fetch API).

## 🚀 Atividades

### 1. Busca de Times (SportsDB API)
Nesta atividade, você desenvolverá uma aplicação que permite buscar informações sobre times de futebol.

- **URL Base:** `https://www.thesportsdb.com/api/v1/json/123/searchteams.php`
- **Parâmetro:** `t` (nome do time)
- **Exemplo de busca:** `https://www.thesportsdb.com/api/v1/json/123/searchteams.php?t=Flamengo`

#### O que deve ser feito:
- Criar um campo de busca para o usuário digitar o nome do time.
- Realizar a requisição utilizando `fetch`.
- Exibir o escudo do time (`strTeamBadge`) e o nome (`strTeam`).

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
- Criar uma interface para digitar a cidade.
- Exibir a temperatura atual (`temp_c`) e a condição climática (`condition.text`).

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
