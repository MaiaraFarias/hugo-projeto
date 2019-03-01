+++
title = "4. Modelo de Dados"
date =  2019-02-11T14:08:44-02:00
weight = 5
+++

<table> 

<td> <b> Afastamento (Complexo) </b> </td>

</tr>

<tr> 

<td> Afastamento {
<p> id: number(20),   
<p> ** numeroServico: string(20),
<p> * inicioAfastamento: date,
<p> * totalDiasAfastado: number (3), 
<p> dataRetorno: date, 
<p> * motivoAfastamento: string(3),
<p> *** cat: {
<p> id: number (20)
<p> }
<p> * mesmoMotivoAnterior: boolean,
<p> tipoAcidenteTransito: number (1),
<p> horaSaida: string (5) // XX:XX
<p> horaRetorno: string (5) // XX:XX
<p> maior15Dias: boolean,
<p> afastamentoDefinitivo: boolean,
<p> observacoes: string (400),
<p> observacoesEsocial: string (400),
<p> * cidCodigo: string (5),
<p> * cidDescricao: string(300),
<p> atestadoExterno: boolean,
<p> alerta: boolean,
<p> nomeUnidadeAtendimento: string (80), // Obrigatorio Caso a FLAG “atestadoExterno” esteja marcada.
<p> cidadeUnidadeAtendimento: string(80), // Obrigatorio Caso a FLAG “atestadoExterno” esteja marcada.
<p>
<p> nomeProfissionalExterno: string(80), // Obrigatorio Caso a FLAG “atestadoExterno” esteja marcada.
<p> orgaoProfissionalExterno: string(1), // Obrigatorio Caso a FLAG “atestadoExterno” esteja marcada.
<p> ufOrgaoProfissionalExterno: string(2), // Obrigatorio Caso a FLAG “atestadoExterno” esteja marcada.
<p> inscricaoProfissionalExterno: number(14), // Obrigatorio Caso a FLAG “atestadoExterno” esteja marcada
<p> 
<p> cidade: string(30) // Obrigatorio Caso a FLAG “atestadoExterno” NÃO esteja marcada
<p> **** unidadeAtendimento: { // schema - Obrigatório Caso a FLAG “atestadoExterno” NÃO esteja marcada.
<p> id: number (20)
<p> }
<p> **** profissionalAtestado: { // schema - Obrigatório Caso a FLAG “atestadoExterno” NÃO esteja marcada
<p> id: number (20)
<p> },
<p> classificacaoInterna: { // schema
<p> id: number (20)
<p> },
<p> pessoa: { // schema
<p> id: number (20)
<p> },
<p> responsavelRegistro: { // schema, usuario logado na aplicacao
<p> id: number (20)
<p> },
<p> **justificativaAtualizacao: string (150)
<p> ** responsavelAtualizacao: { // schema, usuario logado na aplicacao
<p> id: number (20)
<p> },
<p> *1 origemRetificacao : string(20),
<p> *1 tipoProcesso: number(1),
<p> *1 numeroProcessoBeneficio: number(40)
<p> }
<p> <b> Opções: </b>
<p> <b> tipoAcidenteTransito </b>
<p> 1 = Atropelamento
<p> 2 = Colisão
<p> 3 = Outros
<p> <b> orgaoProfissionalExterno </b>
<p> 1 = CRM
<p> 2 = RMS
<p> 3 = CRO
<p> <b> motivoAfastamento </b>
<p> 01 = Acidente/Doença do trabalho
<p> 03 = Acidente/Doença não relacionada ao trabalho
<p> 05 = Afastamento/licença prevista em regime próprio (estatuto), sem remuneração
<p> 06 = Aposentadoria por invalidez
<p> 07 = Acompanhamento - Licença para acompanhamento de membro da família enfermo
<p> 08 = Afastamento do empregado para participar de atividade do Conselho Curador do FGTS - art. 65, §6º, Dec. 99.684/90 (Regulamento do FGTS)
<p> 10 = Afastamento/licença prevista em regime próprio (estatuto), com remuneração
<p> 11 = Cárcere
<p> 12 = Cargo Eletivo - Candidato a cargo eletivo - Lei 7.664/1988. art. 25°, parágrafo único – Celetista sem geral
<p> 13 = Cargo Eletivo - Candidato a cargo eletivo - Lei Complementar 64/1990. art. 1°, inciso II, alínea 1- Servidor público, estatutário ou não, dos órgãos ou entidades da Administração Direta ou Indireta da União, dos Estados, do Distrito Federal, dos Municípios e dos Territórios, inclusive das fundações mantidas pelo Poder Público.
<p> 15 - Gozo de férias ou recesso - Afastamento temporário para o gozo de férias ou recesso
<p> 16 - Licença remunerada - Liberalidade da empresa ou Acordo/Convenção Coletiva de Trabalho
<p> 17 - Licença Maternidade - 120 dias
<p> 18 - Licença Maternidade - a partir de 120 dias até 180 dias
<p> 19 - Licença Maternidade - Afastamento temporário por motivo de aborto não criminoso
<p> 20 - Licença Maternidade - Afastamento temporário por motivo de licença-maternidade decorrente de adoção ou guarda judicial de criança
<p> 22 - Mandato Eleitoral - Afastamento temporário para o exercício de mandato eleitoral, sem remuneração
<p> 23 - Mandato Eleitoral - Afastamento temporário para o exercício de mandato eleitoral, com remuneração
<p> 25 - Mulher vítima de violência - Lei 11.340/2006 - art. 9º §2o, II - Lei Maria da Penha
<p> 26 - Participação de empregado no Conselho Nacional de Previdência Social-CNPS (art. 3º, Lei 8.213/1991)
<p> 27 - Qualificação - Afastamento por suspensão do contrato de acordo com o art 476-A da CLT
<p> 28 - Representante Sindical - Afastamento pelo tempo que se fizer necessário, quando, na qualidade de representante de entidade sindical, estiver participando de reunião oficial de organismo internacional do qual o Brasil seja membro
<p> 29 - Serviço Militar - Afastamento temporário para prestar serviço militar obrigatório;
<p> 30 - Suspensão disciplinar - CLT, art. 474
<p> 31 - Servidor Público em Disponibilidade
<p> Transferência para prestação de serviços no exterior em período superior a 90 dias'
<p> <b> * </b> Obrigatório
<p> <b> ** </b> Obrigatório em caso de edição (PUT)
<p> <b> *** </b> Obrigatório quando o campo “motivoAfastamento” for preenchido com a opção “01”
<p> <b> **** </b> Obrigatório Caso a FLAG “atestadoExterno” NÃO esteja marcada.
<p> <b> *1 </b> Obrigatório apenas em caso de edição e de mudança do motivo de função entre os valores 01 e 03 ou 03 e 01

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Turno (Simples) </b> </td>

</tr>

<tr> 

<td> Turno {
<p> id: number (20), 
<p> status: string(1),
<p> codigo: string(8),
<p> descricao: string(80),
<p> }

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Turno (Completo) </b> </td>

</tr>

<tr> 

<td> Turno {
<p> id: number (20), 
<p> status: string(1),
<p> codigo: string(12),
<p> descricao: string(60),
<p> areas : [
<p> {
<p> id: number(20)
<p> }
<p> ]// schema
<p> }

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Risco (Simples) </b> </td>

</tr>

<tr> 

<td> Risco {
<p> id: number (20), 
<p> codigo: string(8),
<p> descricao: string(80),
<p> esocial:string(10)
<p>  }

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> EpiESocial (Simples) </b> </td>

</tr>

<tr> 

<td> Risco {
<p> ** id: number(20), 
<p> * matricula: number (20), 
<p> * cpf: string (15),
<p> * ca: string(10),
<p> * eficaz: boolean,
<p> * dataInicio: date,
<p> dataFim: date,
<p> * risco:{
<p> id: number(20),
<p> descricao: string (80)
<p> }
<p> }
<p> <b> * </b> Obrigatório
<p> <b> ** </b> Obrigatório em caso de edição;

</td>

</tr>

</table>

<center> <h3> [Início] (/manual-de-integração/modelo-de-dados/modelo-de-dados-4/) <h3> </center>

<center> <h3> <b> [Sumário] (/manual-de-integração/) </b> </center>

