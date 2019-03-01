+++
title = "5. Modelo de Dados "
date =  2019-02-11T14:08:44-02:00
weight = 6
+++

<table> 

<td> <b> GrupoRisco (Lista) </b> </td>

</tr>

<tr> 

<td> Grupo Risco {
<p> id: number(20),   
<p> status: string (1),
<p> codigo: string(8),
<p> descricao: string(100),
<p> exibirAso: boolean,
<p> textoAso: String (200),
<p> restricao: boolean
<p> }

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> GrupoRisco (Complexo) </b> </td>

</tr>

<tr> 

<td> Grupo Risco {
<p> ** id: number(20),
<p> * status: string (1),
<p> * codigo: string(8),
<p> * descricao: string(100),
<p> exibirAso: boolean,
<p> *** textoAso: String (200),
<p> restricao: boolean,
<p> pessoas: [
<p> {
<p> * matriculaPessoa: number(20),
<p> * dataInicio: Date,
<p> dataFim: date,
<p> * matriculaRegistrador: number(20), // o usuário que tem permissão para criar o vinculo
<p> * dataRegistro: date
<p> }
<p> ]
<p>  }
<p> <b> * </b> Obrigatório
<p> <b> ** </b> Obrigatório em caso de edição;
<p> <b> *** </b> Obrigatório caso a flag “exibirAso” esteja marcada.

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> VinculoGrupoRisco (Complexo) </b> </td>

</tr>

<tr> 

<td> <b> * </b> Obrigatório
<p> <b> ** </b> Obrigatório em caso de edição;

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> ASO (Complexo) </b> </td>

</tr>

<tr> 

<td> {
<p> ** id: number(20), 
<p> ** numeroServico: string (12),
<p> * dataASO: date,
<p> * dataAvaliacaoClinica: date,
<p> * tipoASO: number(1),
<p> *** considerarPeriodico: Boolean,
<p> * resultadoASO: number(1),
<p> **** frequencia: number (1),
<p> observacao: string (10000),
<p> descricaoConsulta: string (10000),
<p> * medicoExaminador: {
<p> id: number (20)
<p> },
<p> * medicoCordenador: {
<p> id: number (20)
<p> },
<p> * unidadeAtendimento: {
<p> id: number (20)
<p> },
<p> riscos: [
<p> {
<p> ** id: number (20)
<p> idRisco: number (20),
<p> exibirASO: boolean
<p> }
<p> ],
<p> exames: [
<p> {
<p> ** id: number (20)
<p> idProntuarioExame: number (20),
<p> exibirASO: boolean,
<p> enviarEsocial: boolean
<p> }
<p> ],
<p> grupos: [
<p> {
<p> ** id: number (20)
<p> idGrupo: number(20),
<p> exibirASO: boolean
<p> }
<p> ],
<p> pessoa : {
<p> id: number(20)
<p> }
<p> responsavelRegistro: { // schema, usuario logado na aplicacao
<p> id: number (20)
<p> },
<p> **justificativaAtualizacao: string (150)
<p> ** responsavelCancelamento: { // schema, usuario logado na aplicacao
<p> id: number (20)
<p> },
<p> ***** dataRegistro: date,
<p> ***** dataAtualziacao: date,
<p> ***** dataCancelamento: date
<p> }
<p> <b> Opções: </b>
<p> <b> Tipo ASO </b>
<p> 0 – Admissional
<p> 1 – Periódico
<p> 2 – De Retorno ao Trabalho
<p> 3 – De Mudança de Função 
<p> 8 – Demissional
<p> <b> Resultado ASO </b>
<p> 1 – Apto
<p> 2 – Inapto
<p> <b> Frequência </b>
<p> 3 – 3 Meses
<p> 6 – 6 Meses
<p> 12 – 12 Meses
<p> 24 – 24 Meses
<p>
<p> <b> * </b> Obrigatório
<p> <b> ** </b> Obrigatório em caso de edição;
<p> <b> *** </b> Armazena a informação caso o tipo de ASO seja: 2 ou 3.
<p> <b> **** </b> Obrigatório caso o tipo de aso seja: 0 ou 1
<p> <b> ***** </b> Campo para leitura, toda informacao enviada por aqui sera desconsiderada.


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

<center> <h3> [Início] (/manual-de-integração/modelo-de-dados/modelo-de-dados-5/) <h3> </center>

<center> <h3> <b> [Sumário] (/manual-de-integração/) </b> </center>