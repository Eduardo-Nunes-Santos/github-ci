# GitHub Action - Testando API ViaCEP com Postman

Este projeto configura uma **GitHub Action** para rodar uma **collection do Postman**, testando o endpoint público do [ViaCEP](https://viacep.com.br/).

## 📌 Descrição
O objetivo deste projeto é demonstrar como automatizar testes de API utilizando **GitHub Actions** e **Newman** (CLI do Postman). A collection testada verifica o funcionamento do endpoint:

```
https://viacep.com.br/ws/01001000/json/
```

## 📂 Estrutura do Projeto

```
📦 projeto
 ┣ 📂 .github/workflows
 ┃ ┗ 📜 github-ci.yml  # Configuração da GitHub Action
 ┣ 📂 postman
 ┃ ┗ 📜 viacep-ci.json  # Collection de testes
 ┣ 📜 README.md
```

## ▶️ Executando Localmente
Se quiser testar a collection antes de rodar na Action, siga estes passos:

1. Instale o **Newman**:
   ```sh
   npm install -g newman
   ```
2. Execute os testes:
   ```sh
   newman run postman/viacep-ci.json --reporters cli
   ```

## 📜 Licença
Este projeto é open-source e está disponível sob a licença MIT.

---

### 📌 Observações
- Caso precise adicionar variáveis de ambiente, utilize arquivos `.env` ou configure **secrets** no GitHub Actions.
- Você pode integrar relatórios mais avançados usando o `--reporters html` e armazená-los como artifacts.

