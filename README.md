# ♠️ BlackJack CLI — Jogo de Blackjack em C

> Projeto desenvolvido na disciplina de **Algoritmos e Estruturas de Dados** durante o 1º semestre do curso de **Engenharia de Software**.

---

## 📋 Sobre o Projeto

Implementação de um jogo de **Blackjack (21)** em linguagem C, executado via terminal. O jogo conta com sistema de cadastro e autenticação de jogadores, persistência de dados em arquivo e um ranking atualizado dinamicamente com base no saldo de cada jogador.

---

## 🎮 Funcionalidades

- **Cadastro de jogador** com nome e senha
- **Login** com autenticação por senha
- **Partidas de Blackjack** completas contra o dealer
  - Embaralhamento aleatório do baralho
  - Lógica de Ás valendo 1 ou 11
  - Dealer segue a regra padrão (para em 17+)
  - Sistema de apostas com saldo inicial de R$ 1.000
- **Ranking** dos jogadores ordenado por saldo (maior para menor)
- **Persistência de dados** via arquivo `players.txt`

---

## 🗂️ Estrutura do Projeto

```
blackjack-cli/
├── blackjack.c       # Código-fonte principal
├── players.txt       # Arquivo de dados dos jogadores (gerado automaticamente)
└── README.md
```

---

## 🛠️ Como Compilar e Executar

### Pré-requisitos

- Compilador C (GCC recomendado)
- Terminal Linux, macOS ou Windows (via MinGW/WSL)

### Compilação

```bash
gcc blackjack.c -o blackjack
```

### Execução

```bash
./blackjack
```

---

## 🕹️ Como Jogar

1. Ao iniciar, escolha entre **Registrar** (novo jogador) ou **Fazer Login**
2. Após autenticado, escolha uma das opções do menu:
   - `1` — Iniciar uma partida
   - `2` — Ver o ranking de jogadores
   - `3` — Sair (dados salvos automaticamente)
3. Durante a partida, defina o valor da aposta e decida se deseja **pedir carta** (`s`) ou **parar** (`n`)
4. Vença o dealer sem ultrapassar 21 pontos!

### Regras de Pontuação

| Carta | Valor |
|-------|-------|
| 2 a 10 | Valor nominal |
| Valete, Dama, Rei | 10 |
| Ás | 11 (ou 1, se necessário) |

---

## 👨‍💻 Conceitos de Algoritmos Aplicados

- **Structs** para modelagem de jogadores e resultados
- **Ponteiros** e passagem por referência
- **Manipulação de arquivos** (`fopen`, `fscanf`, `fprintf`)
- **Algoritmo de ordenação** com `qsort` da biblioteca padrão
- **Geração de números aleatórios** com `srand` + `rand`
- **Strings** com `strcmp`, `strcpy`, `strcspn`

---

## ⚠️ Limitações Conhecidas

- Senhas armazenadas em texto puro no arquivo `players.txt`
- Capacidade máxima de 100 jogadores cadastrados
- Sem suporte a múltiplos jogadores simultâneos por rodada

---

## 📚 Disciplina

**Algoritmos e Estruturas de Dados** — 1º Semestre · Engenharia de Software
