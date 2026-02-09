# 📊 Sistema de Gestão de Qualidade – G2L

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-f7df1e?logo=javascript\&logoColor=black)
![Firebase](https://img.shields.io/badge/Firebase-Realtime%20Database-ffca28?logo=firebase\&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-e34f26?logo=html5\&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572b6?logo=css3\&logoColor=white)
![Portfolio](https://img.shields.io/badge/Projeto-Portfolio-blueviolet)

> Sistema web para controle operacional, registro de tempos e acompanhamento de SLA, desenvolvido com **JavaScript** e **Firebase Realtime Database**.

---

## Visão Geral

O **Sistema de Gestão de Qualidade (G2L)** foi criado para registrar e monitorar operações realizadas por operadores, controlando **etapas do processo**, **tempos de execução** e **indicadores de desempenho (SLA)**.
O objetivo principal é garantir **rastreabilidade**, **padronização** e **qualidade** nos processos operacionais.

---

## 🧩 Funcionalidades

* 📌 Cadastro de operações
* ⏱️ Marcação de tempo por etapa
* 👤 Identificação do operador
* 🗂️ Organização por setor
* 📊 Cálculo automático de SLA
* 🔄 Sincronização em tempo real com Firebase
* 🧹 Exclusão de registros
* 📋 Consulta e listagem de operações

---

## 🛠️ Tecnologias Utilizadas

```txt
HTML5        → Estrutura da aplicação
CSS3         → Estilização da interface
JavaScript   → Lógica do sistema
Firebase     → Realtime Database (armazenamento)
```

---

## 🗃️ Estrutura do Projeto

```bash
📁 projeto-g2l
│
├── index.html        # Interface principal
├── style.css         # Estilos da aplicação
├── script.js         # Lógica do sistema
└── README.md         # Documentação
```

---

## 🔄 Fluxo das Etapas

As operações seguem uma ordem lógica pré-definida:

```js
const ordemEtapas = ['entrada', 'checki', 'prep', 'amar', 'checkf', 'saida'];
```

Cada etapa possui um botão para **início/fim de tempo**, permitindo calcular a duração total do processo.

---

## ⏱️ Controle de Tempo

A função responsável pela marcação de tempo é:

```js
function marcarTempo(etapa) {
  const agora = new Date();
  tempos[etapa] = agora.toLocaleTimeString();
}
```

Esses tempos são armazenados no Firebase e utilizados para análises posteriores.

---

## 🔥 Integração com Firebase

O sistema utiliza o **Firebase Realtime Database** para salvar e sincronizar dados em tempo real.

Exemplo de estrutura no banco:

```json
{
  "operacoes": {
    "-Nx123": {
      "operador": "Lucas",
      "setor": "Qualidade",
      "entrada": "08:00:00",
      "saida": "08:45:00",
      "sla": "OK"
    }
  }
}
```

---

## ▶️ Como Utilizar

1. Abra o arquivo `index.html` no navegador
2. Preencha os dados da operação
3. Clique nos botões de cada etapa para marcar o tempo
4. Finalize a operação
5. Os dados serão salvos automaticamente no Firebase

---

## 📌 Regras de Negócio

* As etapas devem seguir a ordem correta
* O SLA é calculado com base no tempo total
* Operações incompletas não são salvas
* Cada registro possui um identificador único

---

## 🚀 Melhorias Futuras

* 📈 Dashboard com gráficos
* 📤 Exportação para Excel/PDF
* 🔐 Autenticação de usuários
* 🧠 Relatórios inteligentes
* 📱 Versão mobile responsiva

---

## 👨‍💻 Autor

**Lucas Ferreira**

Desenvolvedor em formação com foco em **Desenvolvimento Web**, **Sistemas de Informação** e **Qualidade de software**.



---

⭐ Se este projeto te ajudou, considere deixá-lo como favorito no repositório!
