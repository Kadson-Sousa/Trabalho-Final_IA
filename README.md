# 🤖 Trabalho Final - Inteligência Artificial

Trabalho final da disciplina de **Inteligência Artificial**.

---

# 📋 Instruções de Execução

## Pré-requisitos

Antes de executar o projeto, certifique-se de possuir:

- Python **3.10** ou superior;
- `pgmpy`;
- `numpy`;
- `pandas`;
- `matplotlib`;
- `networkx`.

Instale todas as dependências com:

```bash
pip install pgmpy matplotlib networkx numpy pandas
```

---

# 📁 Estrutura do Projeto

O diretório do projeto deve conter os seguintes arquivos:

```text
Trabalho-Final_IA/
│── Trabalho de IA.py
│── dados_pacientes_triagem.csv
│── README.md
```

Onde:

- **Trabalho de IA.py** → arquivo principal do sistema;
- **dados_pacientes_triagem.csv** → base de dados simulada utilizada pela Rede Bayesiana.

---

# ▶️ Como Executar

1. Abra um terminal na pasta do projeto.

2. Instale as dependências (caso ainda não estejam instaladas):

```bash
pip install pgmpy matplotlib networkx numpy pandas
```

3. Execute o programa:

```bash
python "Trabalho de IA.py"
```

> Caso utilize **Jupyter Notebook** ou **Google Colab**, basta executar todas as células em sequência.

---

# ⚙️ Funcionamento

Durante a execução, o sistema realiza automaticamente as seguintes etapas:

1. Carrega a base de dados dos pacientes;
2. Discretiza as variáveis clínicas:
   - Febre;
   - Saturação de O₂;
   - Pressão arterial;
   - Frequência cardíaca;
   - Nível de dor;
   - Idade;
   - Doença crônica;
3. Constrói e valida a **Rede Bayesiana**;
4. Realiza inferências para estimar a probabilidade de gravidade dos pacientes;
5. Gera a fila de pacientes utilizando as probabilidades obtidas;
6. Executa e compara as seguintes estratégias de atendimento:
   - **FIFO** (ordem de chegada);
   - **Busca Gulosa** (maior probabilidade de gravidade);
   - **Algoritmo A\*** (cenário reduzido);
7. Exibe os resultados de cada estratégia, incluindo:
   - ordem de atendimento;
   - risco acumulado total.

---

# 🧠 Estratégias Implementadas

| Estratégia | Descrição |
|------------|-----------|
| FIFO | Atendimento por ordem de chegada. |
| Busca Gulosa | Prioriza pacientes com maior probabilidade de gravidade. |
| A* | Busca a sequência de atendimento que minimiza o risco acumulado considerando o tempo de espera. |

---

# 📌 Observações

- O algoritmo **A\*** é executado apenas no cenário com **6 pacientes**, pois seu espaço de busca cresce de forma fatorial, tornando sua execução inviável para filas maiores.

- No cenário com **25 pacientes**, são executadas apenas as estratégias **FIFO** e **Busca Gulosa**, permitindo a comparação com menor custo computacional.

- A integração entre os módulos ocorre por meio da probabilidade de **Gravidade Alta** estimada pela **Rede Bayesiana**, utilizada pelo algoritmo **A\*** para calcular o risco de deterioração associado ao tempo de espera de cada paciente.

---

# 👥 Autores

Trabalho desenvolvido para a disciplina de **Inteligência Artificial**.
| Kadson Rodrigues de Sousa | 567988 |
| Larissa Maciel da Silva | 568393 |
| Sandy Almir Bonfim | 566604 |
| Patrícia Freire Songo | 571421 |

