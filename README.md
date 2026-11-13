# Carteira de ações da empresa

Ferramenta pessoal, **não oficial**, para colaboradores do grupo VINCI em Portugal acompanharem os seus movimentos num plano de poupança em ações da empresa: compras, bonificações, dividendos e resgates, com cálculo de mais-valias pelo método FIFO e estimativa de imposto.

> Esta ferramenta **não tem qualquer ligação à VINCI, à ANA, à Portway, à Amundi ou à Castor**. Os nomes são usados apenas para indicar a quem se destina e a que se refere. Os valores são estimativas informativas e **não constituem aconselhamento financeiro ou fiscal**: confirme sempre com os extratos oficiais e, se necessário, com a Autoridade Tributária ou um profissional qualificado.

## Como usar

1. Abra a página no navegador (computador ou telemóvel).
2. Importe os seus extratos em PDF (ou cole o texto) na zona «Importar extrato», ou introduza as operações à mão em «Nova operação».
3. Consulte a posição, os resgates, o resumo por ano, os dividendos e a simulação do IRS.
4. Use «Exportar…» para obter um PDF, um ficheiro Excel (.xlsx) ou um CSV.

## Os seus dados

- Tudo corre **no seu navegador**. Os extratos e as operações **não são enviados para lado nenhum** e ficam guardados só neste aparelho.
- Para levar os dados para outro aparelho ou guardar uma cópia, toque no cabeçalho («Modo local…») para abrir **«Os meus dados»** e use **Guardar cópia** e **Carregar cópia**.
- Limpar os dados do navegador, usar um separador privado ou mudar de aparelho começa de novo, a não ser que carregue uma cópia de segurança.


## Cotação automática

Esta versão atualiza a cotação da ação sozinha:

- Uma tarefa agendada do GitHub (`.github/workflows/cotacao.yml`) corre de 10 em 10 minutos, de segunda a sexta, vai buscar a cotação a serviços públicos (Yahoo Finance e, em alternativa, Stooq) e guarda-a no ficheiro `cotacao.json`.
- A página lê o `cotacao.json` de minuto a minuto e mostra o valor na etiqueta do canto superior direito, que diz sempre há quanto tempo foi atualizado.
- **A cotação pode ter atraso** (normalmente 15 a 20 minutos) e **não é oficial**. Se os serviços falharem ou bloquearem o pedido, o ficheiro fica com o último valor e a página mostra-o com a respetiva idade.
- A cotação é **só de leitura**: não se escreve nem se edita em nenhum sítio da página. A cotação aparece **só num sítio**: o valor em destaque do cartão «Cotação VINCI», ao lado do logótipo, que ao tocar abre o painel com os detalhes. Todos os cálculos usam apenas essa cotação.

## Notas

- A cotação da ação é introduzida por si (ou a partir do valor que vê na sua área pessoal da Amundi, em «Conferir com a Amundi»).
- O cálculo da exclusão parcial de mais-valias (art. 43.º, n.º 5 do CIRS) está **desligado por defeito**, porque não está confirmado que este tipo de fundo se enquadre.
- Os relatórios em PDF e Excel usam as bibliotecas jsPDF, jsPDF-AutoTable e SheetJS, carregadas a partir de cdnjs.cloudflare.com.

## Ajuda para quem está a começar

- Na primeira visita pode escolher um **guia passo a passo** ou ir direto ao assunto («Já conheço o plano»). O guia pode ser escondido ou voltar a ser ligado em «Os meus dados».
- Cada termo técnico tem um **ⓘ** com uma explicação curta e uma ligação ao glossário.
- A folha **Simulação** serve para experimentar «e se…» sem alterar os registos reais. Tem um **exemplo com dados fictícios** para aprender a usar a ferramenta.
