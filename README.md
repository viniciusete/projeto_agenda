# projeto_agenda
Projeto da Disciplina de Administração de Banco de Dados Cloud - ETE Paulo Freire


# 📒 Agenda de Contatos com Localização e Relatório de Acessos

Projeto desenvolvido para praticar o uso de bibliotecas JavaScript integradas: **jQuery**, **Axios**, **Day.js** e **Chart.js**.  
O sistema permite cadastrar contatos, buscar endereços via CEP, registrar data/hora e visualizar um gráfico de cadastros.

---

## 🚀 Funcionalidades

- Cadastro de contatos com Nome, Telefone e CEP.
- Busca automática do endereço usando a API ViaCEP.
- Exibição da data e hora da adição de cada contato (formatado com Day.js).
- Lista de contatos cadastrados com possibilidade de exibição dinâmica.
- Gráfico de barras mostrando a quantidade de contatos cadastrados por dia (usando Chart.js).
- Armazenamento dos dados localmente no navegador via `localStorage`.

---

## 🧱 Tecnologias utilizadas

- **HTML / CSS**
- **JavaScript**
- **[jQuery](https://jquery.com/)** – Manipulação do DOM e eventos.
- **[Axios](https://axios-http.com/)** – Consumo da API ViaCEP.
- **[Day.js](https://day.js.org/)** – Manipulação de datas e horas.
- **[Chart.js](https://www.chartjs.org/)** – Criação de gráficos.

---

## 💾 Estrutura dos dados

Cada contato é armazenado no `localStorage` como um objeto com a seguinte estrutura:

```json
{
  "nome": "João Silva",
  "telefone": "83999999999",
  "cep": "58000000",
  "endereco": "Rua Exemplo, Bairro, Cidade - Estado",
  "dataHora": "2025-04-14T14:35:00"
}
```

A lista completa de contatos é salva com a chave **`contatos`**:

```javascript
localStorage.setItem('contatos', JSON.stringify(listaDeContatos));
```

---

## 🗃️ Funcionamento

### 1. Cadastro de Contato
- O usuário preenche Nome, Telefone e CEP.
- Ao digitar o CEP, a aplicação consulta a API ViaCEP e preenche automaticamente o endereço.
- Ao clicar em "Cadastrar", o contato é adicionado à lista e salvo no `localStorage`.

### 2. Exibição dos Contatos
- Os contatos cadastrados são listados abaixo do formulário, com nome, telefone, endereço e data/hora formatados.
- A lista é carregada automaticamente ao abrir a página, a partir do `localStorage`.

### 3. Gráfico de Cadastros
- A cada novo contato cadastrado, o sistema contabiliza a quantidade de cadastros por dia.
- O gráfico é atualizado dinamicamente, exibindo barras para cada dia de cadastro.

### 4. Data e Hora da Última Adição
- No topo da página, a aplicação exibe a data e hora da última adição, atualizada a cada novo contato.

---

## 🧪 Melhorias sugeridas (extras)

- Adicionar a funcionalidade de **remover contatos**.
- Ordenar a lista por ordem decrescente de cadastro (mais recentes no topo).
- Implementar **filtros por data** ou nome.
- Adicionar opção para limpar todos os dados cadastrados.

---

## ⚠️ Observação sobre o Armazenamento

- O `localStorage` é ideal para protótipos e testes, mas não é seguro para armazenar dados sensíveis em aplicações reais.
- O limite de armazenamento gira em torno de 5MB por site.

---
