# Dealer Automation: DANI

O projeto nasceu da necessidade de aumentar a produtividade sem ampliar o quadro operacional. Com a automação de processos é possível alcançar este objetivo reduzindo os custos e liberando o staff para produdir mais, se concentrar em tarefas criativas, estratégicas e dedicar seu tempo à um melhor atendimento aos clientes, fornecedores e colegas de trabalho.

Nossa automação foi batizada de **DANI**, junção das siglas **DN** (Dealer Number) + **AI** (Artificial intelligence).

Em síntese, a DANI é uma coleção de scripts desenvolvidos para automatizar tarefas básicas e recorrentes dentro da concessionária. A automação realizada a atividade e envia um e-mail, diariamente, com o resultado para os responsáveis validarem.

![Video de Introdução](./assets/DANI%20-%20Introdução.mp4)

---

## Nosso processo de automação consiste nas etapas:

- Documentação do processo
- Análise e melhoria do processo
- Desenvolvimento da automação
- Validação

## Os processos já automatizados são:

- **Importação de arquivos diários das montadoras:** A automação acessa o portal da montadora, faz o download dos arquivos de todas as concessionárias do grupo, importa os arquivos no sistema, exporta e organiza os relatórios gerados e envia um e-mail com o resultado. <br>
**Economia de tempo**: 0,5 HHT (hora homem trabalhada) por concessionária

- **Importação das notas fiscais nos portais das seguradoras HDI e Audaparts:** No final do expediente DANI verifica os faturamentos realizados para as seguradoras, acessa o portal e atrela as notas fiscais (PDFs e XMLs) para os processos correspondentes. <br>
**Economia de tempo**: 0,5 HHT por concessionária

- **Cadastro de informações complementares nos veículos:** Após a importação dos veículos faturados a automação realiza o complemento do cadastro do veículos acrescentando informações não importadas pelo DMS mas necessárias para o faturamento do veículo. <br>
**Economia de tempo**: 0,1 HHT por veículo

- **Lançamento de notas de despesas:** O usuário aprovador envia um e-mail com PDF ou XML da nota fiscal informando o rateio e a origem. DANI faz o lançamento da nota fiscal e envia um e-mail para o usuário aprovador com o resultado do lançamento. <br>
**Economia de tempo**: 0,1 HHT por nota fiscal

- **Conciliação do conta corrente:** DANI faz os lançamentos de
    
    - Bônus
    - Holdback
    - Emissão de nota de comissão
    - Baixa de impostos de peças e veículos
      
A automação baixa o arquivo diário e faz os lançamentos que constam no conta corrente, respeitando lançamentos já realizados, adiciona lançamentos não previstos, faz emissão da nota de comissão e baixa dos títulos e adiantamentos. <br>
**Economia de tempo**: 0,5 HHT por concessionária

## Automações em implementação (documentação, análise e desenvolvimento)

- Baixa das propostas de venda direta
- Lançamento da nota fiscal de reparo de usados
- Lançamento de conhecimento de transporte
- Lançamento de notas de veículos e peças
- Geração de GNRE
- Baixa da entrada de veículos seminovos x contas a receber de forma automática

## Automações futuras

- Importação do extrato bancário
- Criação de adiantamento (PIX)
- Lançamento de tarifas
- Baixa automatizada de cartões e títulos
- Integração com Mercado Livre (Criação de atendimento, integração da nota fiscal e baixa do contas a receber)

## Módulos Internos da TI

- **DANI-Manager**  
    Uma interface gráfica avançada desenvolvida em Vue e PywebView, utilizada para depurar a DANI e reexecutar tarefas que falharam de forma gráfica.

- **DANI-Files**  
    Uma interface gráfica simples que permite visualizar os arquivos gerados pela DANI através de um navegador. Isso inclui todos os e-mails e arquivos .pk que a DANI gerou ou baixou da montadora.

- **Gerador de Assinaturas**  
    Um programa com interface gráfica que facilita a criação de assinaturas de e-mail para Thunderbird e Outlook. <br>
    **Economia de tempo**: 0,1 HHT por assinatura

- **Script de Instalação**  
    Um programa modular que executa scripts com base na seleção do usuário. Atualmente, é utilizado para instalar toda a gama de software da empresa com apenas um clique. Graças a essa ferramenta, a equipe de TI consegue configurar um computador recem formatado para pronto para o uso em aproximadamente 15 minutos. <br>
    **Economia de tempo**: 3,5 HHT por equipamento
