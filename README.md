# 🧮 Calculadora Multifuncional

> Fluxograma de uma calculadora com menu de 10 funções, desenvolvido em **Flowgorithm** para aplicar conceitos de lógica de programação, com uma versão estendida em **linguagem C**.

![Ferramenta](https://img.shields.io/badge/Flowgorithm-fluxograma-orange)
![Linguagem](https://img.shields.io/badge/linguagem-C-blue)
![Status](https://img.shields.io/badge/status-concluído-brightgreen)
![Licença](https://img.shields.io/badge/licença-MIT-blue)

## 📌 Visão geral e contexto

Projeto acadêmico desenvolvido em grupo na disciplina **Algoritmos e Pensamento Computacional**, do curso de **Engenharia de Software** (2º semestre de 2026).

O objetivo foi praticar as estruturas básicas da lógica de programação (variáveis, entrada e saída, decisão e repetição) construindo uma ferramenta útil: uma calculadora que reúne, em um único programa, operações matemáticas, cálculos de área e conversão de temperatura, sem que o usuário precise reiniciar o programa a cada cálculo.

### Objetivo

Desenvolver, em Flowgorithm, um fluxograma para uma Calculadora Multifuncional que apresente um menu principal com 11 opções (10 funções de cálculo + a opção de encerrar o programa), permanecendo em execução e retornando sempre ao menu até que o usuário escolha encerrar.

## 👥 Integrantes do grupo

- Julia Rodrigues Bezerra
- Rafael Oliveira
- Roberto Rosado
- Nicole Moreira

## 🛠️ Tecnologias utilizadas

- **[Flowgorithm](http://www.flowgorithm.org/)**: ferramenta gratuita para criar e executar programas em forma de fluxograma
- Funções internas do Flowgorithm: `Sqrt()` e a constante `pi`
- **Linguagem C** (versão estendida), com as bibliotecas `stdio.h`, `stdlib.h` e `math.h`

## ▶️ Como executar

### Fluxograma (Flowgorithm)

**Pré-requisitos:** Windows e o [Flowgorithm](http://www.flowgorithm.org/download/) instalado.

1. Baixe este repositório: clique no botão verde **Code → Download ZIP** e extraia a pasta.
2. Abra o Flowgorithm.
3. Vá em **File → Open** e selecione o arquivo `CalculadoraMultifuncional (1).fprg`.
4. Clique em **Run** (▶) ou pressione **F5**.
5. Na janela do console, digite o número da opção desejada e siga as instruções na tela.

### Versão em C

**Opção 1: no navegador, sem instalar nada**
1. Acesse [onlinegdb.com](https://www.onlinegdb.com/online_c_compiler).
2. Apague o código de exemplo e cole o conteúdo do arquivo `calculadora.c`.
3. Clique em **Run**.

**Opção 2: no computador (com GCC instalado)**
```bash
gcc calculadora.c -o calculadora -lm
./calculadora
```

## ⚙️ Descrição das 10 funções de cálculo (fluxograma)

1. **Soma**: soma dois números reais informados pelo usuário (n1 + n2).
2. **Subtração**: subtrai o segundo número do primeiro (n1 - n2).
3. **Multiplicação**: multiplica dois números reais (n1 * n2).
4. **Divisão**: divide o primeiro número pelo segundo (n1 / n2). Antes de calcular, verifica se o divisor é zero e, nesse caso, exibe uma mensagem de erro.
5. **Potenciação**: eleva uma base a um expoente (base ^ expoente).
6. **Raiz Quadrada**: calcula a raiz com a função `Sqrt`. Se o número for negativo, exibe uma mensagem de erro.
7. **Área do Círculo**: calcula a área a partir do raio, usando `pi` (pi * raio²).
8. **Área do Retângulo**: calcula a área a partir da base e da altura (base * altura).
9. **Celsius para Fahrenheit**: converte a temperatura (F = C * 9/5 + 32).
10. **Média Aritmética**: calcula a média de três números ((n1 + n2 + n3) / 3).
11. **Encerrar**: finaliza o programa, saindo do laço principal.

## ➕ Versão estendida em C

O arquivo `calculadora.c` amplia a ideia do fluxograma para **20 operações**, incluindo resto da divisão, porcentagem, fatorial, número primo, tabuada, maior e menor valor, área, perímetro e volume de várias figuras, Teorema de Pitágoras, equação do 2º grau (Bhaskara), distância entre pontos e conversão entre graus e radianos. Ele também valida a entrada: se o usuário digitar uma letra no lugar de um número, o programa pede o valor de novo em vez de travar.

## 🔄 Lógica de funcionamento (fluxograma)

- A variável `opcao` é inicializada com `0` antes do menu começar.
- Um laço `While (opcao <> 11)` mantém o programa em execução enquanto a opção não for "Encerrar".
- A cada repetição do laço:
  - o menu com as 11 opções é exibido;
  - o programa lê a opção escolhida (`Input opcao`);
  - uma cadeia de `If / Else` (uma para cada opção, de 1 a 11) executa a operação correspondente;
  - se o valor não estiver entre 1 e 11, exibe *"Opção inválida! Digite um número entre 1 e 11."*;
  - ao final, o fluxo volta ao topo do laço e reexibe o menu, exceto na opção 11, quando a condição `opcao <> 11` se torna falsa e o programa encerra.
- Ao sair do laço, o programa exibe *"Programa encerrado."*.

As operações de **Divisão** e **Raiz Quadrada** têm uma segunda camada de decisão interna para tratar entradas inválidas (divisão por zero e raiz de número negativo) antes de calcular.

## 🧱 Estruturas utilizadas

| Estrutura | Onde é usada |
|---|---|
| Variáveis | `opcao` (Integer); `n1`, `n2`, `n3`, `resultado`, `base`, `expoente`, `raio`, `baseRet`, `alturaRet`, `celsius` (Real) |
| Entrada de dados (Input) | Leitura da opção do menu e dos valores de cada operação |
| Saída de dados (Output) | Exibição do menu, das mensagens de erro e dos resultados |
| Repetição (While) | Mantém o menu em execução até a opção 11 |
| Decisão (If/Else) | Identifica a opção escolhida e trata casos especiais (divisão por zero, raiz negativa, opção inválida) |
| Atribuição (Assign) | Cálculo do resultado de cada operação |
| Funções internas | `Sqrt()` (raiz quadrada) e `pi` (área do círculo) |

## 📁 Estrutura do repositório

```
├── CalculadoraMultifuncional (1).fprg   # fluxograma do Flowgorithm
├── calculadora.c                        # versão estendida em C
├── LICENSE
├── .gitignore
└── README.md
```

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](./LICENSE) para mais detalhes.ais detalhes.
