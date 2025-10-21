# Sprint-4---XP---QA

# XP2 – Extensão Anti-Apostas (Back-end)

**Integrantes**  
- Lucca Alexandre – 99700  
- Victor Wittner – 98667  
- Matheus Haruo – 97663  
- João Saborido – 98184  

## 🔗 Links da Entrega
- **Azure Boards (Plano de Testes – Parte A):** (https://dev.azure.com/RM98667/Sprint%202%20-%20QA)
- **Relatório de execução (Newman):** `docs/automation-report/index.html` 

## 🧩 Parte A – Plano de Testes no Azure Boards
- Casos de teste registrados como **Tasks** vinculadas aos respectivos **PBIs**.
- Cada Task contém: **Dados de entrada**, **Dados de saída esperados**, **Passos**, **Resultados esperados**.
- Evidências (prints): `docs/azure-boards-evidencias/`.

## 🤖 Parte B – Automação com Postman
Coleção e environment:
- `postman/collection.json`
- `postman/env.json` (usar `baseUrl`, ex.: `http://localhost:3000`)

### Executando no Postman
1. Importar `postman/collection.json`.  
2. Criar Environment com `baseUrl`.  
3. Run → verificar todos os testes verdes.

### Executando via Newman
```bash
npm i -g newman newman-reporter-htmlextra
newman run postman/collection.json -e postman/env.json -r cli,htmlextra
# relatório em docs/automation-report/
