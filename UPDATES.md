# [ATUALIZAÇÕES:](./UPDATES.md#vers%C3%A3o-10---06122023)

## VERSÃO 1.7 - 14/08/2025
* ✅ **MODO 0:** Agora não só **adiciona zeros**, mas também **remove zeros**, transformando, por exemplo, `"01"` em `"1"` e `"002"` em `"2"`, sempre respeitando a quantidade mínima de dígitos definida pelo slider (`self.var_zeros`).
---

## VERSÃO 1.6 - 24/07/2025
* ✅**Novo botão AJUDA:** Adicionado ao lado do botão **SELECIONAR**, este botão abre automaticamente o navegador padrão e direciona o usuário para a documentação oficial do modo de renomeação atualmente selecionado. Isso permite esclarecer dúvidas de forma rápida e consultar exemplos práticos sobre o funcionamento de cada modo. É necessário estar conectado à internet, pois os links levam ao `README.md` do repositório no GitHub.
* ✅**Melhoria no layout dos botões:** Os botões **RENOMEAR** e **RESETAR** agora aparecem lado a lado.
---

## VERSÃO 1.5 - 23/07/2025
* ✅**MODO GERAL:** Agora o Modo `GERAL` **modifica corretamente tanto os prefixos quanto os sufixos dos nomes**.
Ou seja, ele entende quando o nome universal é um número com um separador (como `05-`, `05)`, etc) e usa isso como base para numerar os arquivos dinamicamente. Exemplos:

| NOME UNIVERSAL | ARQUIVOS RENOMEADOS      |
| --------------------------------- | ----------------------- |
| `-`                               | `01-SONG`, `02-VALOR`   |
| `05-`                             | `05-SONG`, `06-VALOR`   |
| `)`                               | `01) SONG`, `02) VALOR` |
| `05)`                             | `05) SONG`, `06) VALOR` |
| `_`                               | `01_SONG`, `02_VALOR`   |
| `05_`                             | `05_SONG`, `06_VALOR`   |
| `$`                               | `01 SONG`, `02 VALOR`   |
| `05$`                             | `05 SONG`, `06 VALOR`   |

> 💡 **Importante:** O caractere `$` não é inserido nos nomes dos arquivos — ele apenas representa que será usado um **espaço em branco** entre o número e o nome original.
* ✅**MODO 0:** Esse modo agora **detecta automaticamente números no início ou fim dos nomes dos arquivos** e os **padroniza com zeros**, conforme a quantidade de dígitos definida no controle deslizante (ex: 3 dígitos → `001`, `045`, etc).
---

## VERSÃO 1.4 - 14/06/2025
* ✅**Controles de ordenação visíveis apenas no modo GERAL:** Os botões de ordenação e o switch de ordem agora só aparecem e funcionam quando o modo GERAL está selecionado.
* ✅**Seção de zeros à esquerda (modo `0`):** Ao selecionar o modo `0`, uma nova seção é exibida acima do botão "RENOMEAR", contendo o controle `QUANTIDADE` — um *slider* que vai de 1 a 9. Esse controle permite definir o número total de dígitos desejado nos números finais dos nomes dos arquivos. O valor padrão é 3 dígitos.
* ✅**Botão RESETAR:** Permite desfazer a última renomeação realizada, restaurando os nomes originais dos arquivos. Não feche o aplicativo ou inicie uma nova renomeação, senão a ação de resetar será perdida.
---

## VERSÃO 1.3 - 09/06/2025
* ✅**Numeração inteligente:** Agora, se o nome universal terminar com um número, a numeração sequencial começará a partir desse número, mantendo os zeros à esquerda.  
  Exemplo: FAIXA 05 → FAIXA 05, FAIXA 06, FAIXA 07...

  * ✔️Também funciona nos seguintes casos:
    * Quando o nome universal é apenas um número:  
      Exemplo: 05 → 05.ext, 06.ext, 07.ext...
    * Quando o campo está em branco:  
      Resultado: 01.pdf, 02.png, 03.docx...

* ✅Arquivos ocultos e de sistema são ignorados automaticamente durante o processo de renomeação — mesmo que estejam visíveis no Explorador do Windows.
* ✅O nome do aplicativo foi alterado de "RENOMEAR ARQUIVOS" para "RENOMEADOR DE ARQUIVOS".
---

## VERSÃO 1.2 - 21/05/2025
* ✅Este aplicativo agora utiliza a biblioteca `customtkinter` para uma interface gráfica mais moderna e estilizada, substituindo o antigo `tkinter`. 
* ✅Foi adicionado um novo botão chamado `MISTO`, que renomeia os arquivos convertendo apenas a primeira letra de cada nome para maiúscula.
---

## VERSÃO 1.1 - 20/05/2025:
* ✅O aplicativo agora se chama "RENOMEAR ARQUIVOS".
* ✅Foi criado o instalador.
* ✅Renomeia arquivos com 4 modos: `GERAL` (ordem por ID3), `0` (adiciona "0"), `UPPER` e `LOWER`. Campo "NOME UNIVERSAL" aparece só no modo `GERAL`. Feedback via pop-ups.
* ✅Os aplicativos apagados foram: "RENOMEAR PARA 0" e "RENOMEAR UPPER" -> (06/12/2023).
---

## VERSÃO 1.0 - 06/12/2023:
* ✅**O aplicativo é lançado oficialmente com o nome `RENOMEAR MUSICAS`, desenvolvido com `tkinter`:**
A interface conta com um botão "SELECIONAR", utilizado para escolher o diretório, um campo para inserir o nome universal (aceitando apenas um parâmetro) e o botão "RENOMEAR".
Uma `messagebox` é exibida ao final do processo, indicando se a renomeação foi bem-sucedida ou se ocorreu algum erro.
* ✅**Em `18/12/2023`, foram feitas algumas melhorias no aplicativo (1.0.1):**
  * 🔹Adição de um rodapé com meu nome e meu username do GitHub.
  * 🔹Refatoração e revisão do código para maior clareza e eficiência.
  * 🔹Inclusão do nome e do ícone oficial do aplicativo.
  * 🔹Alteração no parâmetro de compilação, eliminando a necessidade de o usuário ter pacotes do módulo `_internal` instalados no sistema. Agora, o aplicativo é totalmente autônomo.



