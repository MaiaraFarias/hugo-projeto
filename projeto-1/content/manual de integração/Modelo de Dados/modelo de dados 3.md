+++
title = "Modelo de Dados 3"
date =  2019-02-11T14:08:44-02:00
weight = 4
+++


</table>

<br>

<table>

<tr>

<td> <b> GHE  (Detalhe) </b> </td>

</tr>

<tr> 

<td> GHE: {
<p> id: number(20), 
<p> codigo: string(8),
<p> descricao: string(100),
<p> expostos: number(3),
<p> revezamento: string(10),
<p> jornadaDiaria: number(2,1),
<p> jornadaSemanal: number(2,1),
<p> localTrabalho: string(999),
<p> dataInicio: date,
<p> dataFim: date,
<p> estabelecimentoTerceiro: boolean,
<p> cnpjTerceiro: string(14),
<p> dataAtualizacao: date, // informa quando foi a ultima alteracao feita no ghe
<P> area1: {
<p> id: number(20),
<p> codigo: string(8)
<p> descricao: string(60)
<p>} },
<p> area2: {
<p> id: number (20)
<p> codigo: string(8),
<p> descricao: string(60)
<p> },
<p> area3: {
<p> id: number(20),
<p> codigo: string(8),
<p> descricao: string(60)
<p> },
<p> cargos: [
<p> {
<p> id: number(20),
<p> descricao: string(100),
<p> }
<p> ],
<p> atividades: [
<p> {
<p> id: number(20),
<p> descricao: string(100),
<p> frequencia: string(1), // E = Eventual | H = Habitual
<p> dataFim: date,
<p> dataInicio: date,
<p> sequencia: number(1),
<p> ppp: boolean
<p> }
<p> ],
<p> riscosGhes: [
<p> {
<p> id: number(20),
<p> risco: {
<p> id: number(20),
<p> codigo: Q004,
<p> descricao: string(100),
<p> esocial:string(10)
<p> }
<p> probabilidadePPRA: {
<p> id: number(20),
<p> descricao: string(200),
<p> },
<p> severidadePPRA: {
<p> id: number(20),
<p> descricao:  string(200),
<p> },
<p> nivelRiscoPPRA: {
<p> id: number(20),
<p> descricao:  string(200),
<p> },
<p> dataInicio: date,
<p> dataFim: date,
<p> viaAbsorcao:  string(2),  // D = Dérmica | R = Respiratória | DR = Dérmica e Respiratório
<p> frequenciaExposicao:  string(1), // E = Eventual | H = Habitual
<p> raCabeca: boolean,
<p> raOlhos: boolean,
<p> raTronco: boolean,
<p> raMembrosInferiores: boolean,
<p> raMembrosSuperiores: boolean,
<p> raPele: boolean,
<p> raSistemaAuditivo: boolean,
<p> medidasControlesRiscosGhes: [
<p> {
<p> id: number(20),
<p> eficaz: boolean,
<p> dataInicio: date,
<p> dataFim: date,
<p> epi: {
<p> codigo: number(20),
<p> descricao: string(100),
<p> }
<p> }
<p> ],
<p> fontesGeradoras: [
<p> {
<p> id: number(20),
<p> descricao: string(100),
<p> }
<p> }
<p> ],
<p> recomendacoes: [
<p> {
<p> id: number(20),
<p> recomendacao: string(100)
<p> dataInicio: date,
<p> dataFim: date,
<p> }
<p> ]
<p> }
<p> ],
<p> insalubridade : [
<p> {
<p> id: number(20),
<p> fatorRisco: {
<p> id: number(20),
<p> 
<p> },
<p> grau: number (2),
<p> dataInicio: date,
<p> dataFim: date
<p> }
<p> ],
<p> periculosidade : [
<p> {
<p> id: number(20),
<p> fatorRisco: {
<p> id: number(20),
<p> descricao: string(100)
<p> },
<p> dataInicio: date,
<p> dataFim: date
<p> }
<p> ],
<p> aposentadoriaEspecial : [
<p> {
<p> id: number(20),
<p> fatorRisco: {
<p> id: number(20),
<p> descricao: string(100)
<p> },
<p> codigoFAE: number (2),
<p> dataInicio: date,
<p> dataFim: date
<p> }
<p> ],
<p> gfip : [
<p> {
<p> id: number(20),
<p> gfip: number (2),
<p> dataInicio: date,
<p> dataFim: date
<p> }
<p> ]
<p>
<p> }



</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> CalculoEstatisticoGHE </b> </td>

</tr>

<tr> 

<td> CalculoEstatisticoGHE

<p>  ghe: {

<p> id: number(20), 

<p> codigo: String(8),  

<p> descricao(100) 

<p> },

<p> calculos: [ 

<p> id: number(20),

<p> tipoAvaliacao: String(10), // verificar lista de opções

<p> resultadoCalculo: String(20),

<p> unidadeMedida: String(20),
      
<p> unidadeMedida: String(20),
    
<p> nenQ3: String(10),
    
<p> nemQ5: String(10),
    
<p> tecnicaMedicao: String(60),
    
<p> parametroSelecionado: String(10)// verificar lista de opções
    
<p> dataInicio: Date,
    
<p> dataFim: Date,

<p> nivelRiscoLegal: {

<p> id: number(20),

<p> descrição: String(60)

<p> }

<p> nivelRiscoTecnico: {

<p> id: number(20),

<p> descrição: String(60)

<p> }

<p> risco: {

<p> id: number(20),

<p> codigo: String(20),

<p> descricao: String(200),

<p> esocial: String(20)

<p> }

<p> ]

<p> }

<p> <b> TipoAvaliacao </b>

<p> TLV/TWA

<p> VDVR

<p> Aren

<p> IBUTG

<p> STEL

<p> Ceiling

<p> <b> ParametroSelecionado </b>

<p> MEV = Menor Valor

<p> MAV = Maior Valor

<p> MP = Media Ponderada

<p> MG = Media Geométrica

<p> MA = Media Aritmética

<p> LIC = Limite Inferior de Confiança

<p> LSC = Limite Superior de Confiança

<p> 95 = Percentil 95

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Profissional  (Simples) </b> </td>

</tr>

<tr> 

<td> Profissional {
<p> id: number (20),  
<p> nome: string (80)
<p>  }

</td>

</tr>

<br>

<table>

<tr>

<td> <b> CAT (Simples) </b> </td>

</tr>

<tr> 

<td> CAT {
<p> id: number (20),  
<p> numeroCat: string (20),
<p> dataAcidente: date
<p>  }

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Afastamento (Simples) </b> </td>

</tr>

<tr> 

<td> Afastamento {
<p> id: number (20),   
<p> status: string (2),
<p> dataRegistro: date,
<p> dataAtualizacao:date,
<p> motivoAfastamento: string(3),
<p> mesmoMotivoAnterior: boolean,
<p> horaSaida: string (5) // XX:XX
<p> horaRetorno: string (5) // XX:XX
<p> cidCodigo: string (5),
<p> cidDescricao: string(300),
<p> atestadoExterno: boolean,
<p> centroMedico: {
<p> id: number (20),
<p> descricao: string (110)
<p> }
<p> pessoa: {
<p> id: number (20),
<p> matriculaEmpresa: string (20),
<p> nome: string (60)
<p> },
<p> responsavelRegistro: {
<p> id: number (20),
<p> matriculaEmpresa: string (20),
<p> nome: string (60)
<p> },
<p> profissionalAtestado: {
<p> id: number (20),
<p> nome: string (80)
<p> }
<p> 
<p> }


</td>

</tr>

</table>

<br>

<table>

<tr>

<center> <h3> [Início] (/manual-de-integração/modelo-de-dados/modelo-de-dados-3/) <h3> </center>






