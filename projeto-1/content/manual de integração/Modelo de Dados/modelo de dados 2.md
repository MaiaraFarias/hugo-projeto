+++
title = "2. Modelo de Dados "
date =  2019-02-11T14:08:44-02:00
weight = 3
+++


</table>

<br>

<table>

<tr>

<td> <b> 
PessoaLider  (Simples) </b> </td>

</tr>

<tr> 

<td> PessoaLider {
<p> id: number (20, 
<p> matriculaEmpresa: string (20),
<p> status: string (1),
<p> nome: string (60),
<p> dataNascimento: date
<p> sexo: string (1),
<p> rg: string (15),
<p> orgaoExpeditorRG: string (8),
<p> ufOrgaoExpeditorRG: string (8),
<p> cargo: {
<p> id: number (20)
<p>},
<p> ghe: {
<P> id: number (20)
<p>},
<p> area1: {
<p> id: number (20)
<p>},
<p> area2: {
<p> id: number (20)
<p> },
<p> area3: {
<p> id: number (20)
<p> }
<p> }

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Pessoa (Complexo) </b> </td>

</tr>

<tr> 

<td> Pessoa {

<p>  **id: number (20), 

<p> * matriculaEmpresa: string (20), 

<p> * status: string (1),  

<p> * nome: string (60), 

<p> * cpf: string (11), 

<p>* rg: string (15), 

<p> email: string (60),

<p> foneFixo: number (11),

<p> foneCelular: number (11), 

<p> * dataAdmissao: date, 
      
<p> dataDemissao: date,
    
<p> * dataNascimento: date, 
    
<p> dataEmissaoRg: date, 
    
<p> tipoFuncionario: string (1),
    
<p> * sexo: string (1),
    
<p>  nit: string (14), // Numero de inscrição do segurado
    
<p> orgaoExpeditorRG: string (8), 

<p> ufOrgaoExpeditorRG: string (8),

<p> ctps: string (8),

<p> serie: string (5),

<p> * uf: string (2), 

<p> * brPdh: string (3),

<p> regimeTrabalho: string (15) // Regime de Revezamento de Trabalho, para trabalhos em turnos ou escala

<p> cbo: number (20),

<p> podeLiderar: boolean,

<p> cep: string (8),

<p> logradouro: string (100),

<p> cidade: string (60),

<p> ufEstado: string(2),

<p> tipoSanquineo: number (2),

<p> líder: {

<p> id: number (20)

<p> },

<p> V01 turno: {

<p> id: number (20)

<p> },

<p> centroCusto: {

<p> id: number (20)

<p> },

<p> cargo: {

<p> id: number (20)

<p> },

<p> #***** ghe: {

<p> id: number (20)

<p> },

<p> * area1: {

<p> id: number (20)

<p> },

<p> area2: {

<p> id: number (20)

<p> },

<p> area3: {

<p> id: number (20)

<p> },

<p> ***** historico: [

<p> {

<p> * dataInicio: string(),

<p> dataFim: string(),

<p> idArea1: number(20),

<p> idArea2: number(20),

<p> idArea3: number(20),

<p> idCargo: number(20),

<p> idGhe: number(20),

<p> cbo: number(20),

<p> gfip: string(2)

<p> }

<p> ],

<p> ***dataAtualizacao: date,

<p> **** limparHistorico: Boolean

<p> }

<p> <b> Opções </b> 

<p> <b> status: </b> 

<p> A = Ativo

<p> I = Inativo

<p> C = Candidato

<p> <b> tipoFuncionario </b>

<p> T = Terceiro

<p> F = Funcionario

<p> <b> Sexo </b>

<p> M = Masculino

<p> F = Feminino

<p> <b> brPdh </b>

<p> BR = Beneficiário Reabilitado

<p> PDH = Portador de Deficiência Habilitado

<p> NA = Não Aplicável

<p> <b> tipoSanguineo </b>

<p> 1 = A+

<p> 2 = A-

<p> 3 = B+

<p> 4 = B-

<p> 5 = AB+

<p> 6 = AB-
 
<p> 7 = O+

<p> 8 = O-

<p> <b> * </b>  Obrigatório

<p> <b> ** </b>  Obrigatório em caso de edição (PUT)

<p> <b> *** </b>  Este campo informa uma DATA a ser usada como inicio/fim na geração do histórico no cadastro de pessoas.

<p> <b> **** </b> Informando TRUE no campo limparHistorico o Apollus apaga todo o historico cadastrado e gera novamente um historico baseado nos dados atuais.

<p> <b> ***** </b> Populando o atributo “historico” o Apollus altera o modo com que é gerado o Historico de Pessoa, levando como base os dados informado no atributo.

<p> <b> V01 </b> Se não for informado uma área nivel1 a informação vinculada ao campo sera ignorada.

<p> <b> # </b> Este campo aceita a realização de merge das informações, ou seja, se informado o valor CHAVE {id: 0} no objeto o Integrador entende que este campo não deve apagar as informações já contidas nele. Cenario: Valores onde foram inseridos manualmente pelo Sistema Apollus e a informação não existe por parte do consumidor do WS.

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> GHE  (Simples) </b> </td>

</tr>

<tr> 

<td> GHE {
<p> id: number (20),  
<p> codigo: string (20),
<p> descricao: string (80),
<p> dataAtualizacao: date, // informa quando foi a ultima alteracao feita no ghe
<p> area1:{
<p> id: number (20),
<p> descricao: string (60)
<p> }
<p> area2:{
<p> id: number (20),
<p> descricao: string (60)
<p> }
<p> area3:{
<p> id: number (20),
<p> descricao: string (60)
<p> }
<p> }

</td>

</tr>

<br>

<table>

<tr>

<td> <b> GHE  (Complexo) </b> </td>

</tr>

<tr> 

<td> GHE {
<p> ** id: number (20),  
<p> * codigo: string (20),
<p> * descricao: string (80),
<p> * jornadaDiaria: number (2,1),
<p> * jornadaSemanal: number (2,1),
<p> * revezamento: string (15),
<p> * localTrabalho: string(999),
<p> * dataIncio: date,
<p> * dataFim: date,
<p> * cargos: [ // schema Cargo
<p> {
<p> id: number (20)
<p> }
<p> ],
<p> *area1: { // schema Area
<p> id: number (20)
<p> },
<p> *area2: { // schema Area
<p> id: number (20)
<p> },
<p> *area3: { // schema Area
<p> id: number (20)
<p> }
<p>
<p> }
<p> <b> * </b> Obrigatório
<p> <b> ** </b> Obrigatório em caso de edição (PUT)


</td>

</tr>

</table>

<center> <h3> [Início] (/manual-de-integração/modelo-de-dados/modelo-de-dados-2/) <h3> </center>

<center> <h3> <b> [Sumário] (/manual-de-integração/) </b> </center>