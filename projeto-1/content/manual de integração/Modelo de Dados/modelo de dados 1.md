+++
title = "1. Modelo de Dados "
date =  2019-02-11T14:08:44-02:00
weight = 2
+++

<table>

<tr>

<td> <b> Área (Simples) <b> </td>

</tr>

<tr> 

<td> Area { // Hierarquia 1
<p> id: number (8), 
<p> status: string (1),
<p> codigo: string (8),
<p> descricao: string (60
<p> areasFilhas: [// Hierarquia Nivel 2
<p> id: number (8)
<p> status: string (1),
<p> codigo: string (8),
<p> descricao: string (60)
<p> areasFilhas: [// Hierarquia Nivel 3
<p> id: number (8), 
<p> status: string (1),
<p> codigo: string (8),
<p> descricao: string (60)
<p> ]
<p> ]
<p> }

</td 

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Área (Simples 2) <b> </td>

</tr>

<tr> 

<td> Area { // Hierarquia 1
<p> id: number (8), 
<p> status: string (1),
<p> codigo: string (8),
<p> descricao: string (60
<p> }

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Area (Complexa) <b> </td>

</tr>

<tr> 

<td> Area {

<p>**** id: number (8),

<p>* status: string (1),

<p>* codigo: string (8),

<p>* descricao: string (60),

<p>* codigoHierarquia: number (1),

<p>* nomeFantasia: string (60),

<p>* tipoInscricao: number (1), // 1 = CNPJ | 2 = CPF

<p>inscricao: string(18),

<p>entidadeAdministracaoPublica: boolean,

<p>cnaeCodigo: string (10),

<p>cnaeDescricao: string (200),

<p>cep: string (8),

<p>cidade: string(30),

<p>uf: string(2),

<p>complemento: string (100),

<p>telefone: number (11),

<p>observacoes: string (200),

<p>grauRisco: number (1),

<p>numeroFuncionarios: number (3),

<p>grupoCipa: string (20),

<p>endereço: string(80),

<p>numero: numérico(3),

<p>*** idPai: number (20)

<p>**centroCusto: {

<p>id: number (20)

<p>}
<p>}

<p> <b> Opções:</b>


<p> <b> status: </b>
    

<p> A = Ativo
    
<p> I = Inativo
    

<p> <b> grauRisco: </b>
    

 <p> 1
    
 <p> 2
    
 <p> 3
    
 <p>  4
    

<p> <b> codigoHierarquia </b>
    

<p>  1 = Nível 1
    
<p>  2 = Nível 2
    
<p>  3 = Nível 3
    
<p>  idPai
    

<p> <b> * </b> Obrigatório

<p><b> ** </b> Campo não obrigatório, contudo caso seja informado o mesmo deve referenciar um ID (código interno do apollus) de um Centro de Custo cadastro no Apollus.

<p><b> *** </b> idPai: Caso esteja sendo criado uma Área de nível 2 ou 3 é obrigatório informar o ID (Codigo Interno Apollus) da Área nível 1.

<p> <b> **** </b> Obrigatório em caso de edição (PUT)


</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Cargo (Simples) </b> </td>

</tr>

<tr> 

<td> Cargo {
<p> id: number (8), 
<p> status: string (1),
<p> descricao: string (60)
<p> }


</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> Cargo (Complexo) </b> </td>

</tr>

<tr> 

<td> 
Cargo {

<p>  id: number (8),

<p> * status: string (1), // A = Ativo |I = Inativo

<p>* codigo: string (8),

<p>* descricao: string (60),

<p>potencialmentePericuloso: boolean,

<p>** referencia: number (1), // 1 = Bombeiro | 2 = Motocicleta |3 = Segurança Pessoal

<p>atividades: string(400)

<p>}

<p> <b> Opções: </b>

<p> <b>   status: </b>
    
    
<p>  A = Ativo </b>
    
<p>   I = Inativo </b>
    
<p> <b>   referencia: </b>
    
<p>  1 = Bombeiro
    
<p>  2 = Motocicleta
    
<p>  3 = Segurança Pessoa
    

<p> <b> * </b> Obrigatório 

<p> <b> ** </b>Obrigatório caso o campo “potencialmentePericuloso” esteja marcado.

<p> <b> *** </b> Obrigatório em caso de edição (PUT)


</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> CentroCusto (Simples) </b> </td>

</tr>

<tr> 

<td> CentroCusto {
<p> id: number (8), 
<p> status: string (1),
<p> codigo: string (8),
<p> descricao: string (60)
<p> }


</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> EPI (Simples) </b> </td>

</tr>

<tr> 

<td> EPI {
<p> id: number (8), 
<p> status: string (1),
<p> descricao: string (60),
<p> categoria: string (2),
<p> classe: string (2)
<p> }


</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> EPI (Complexo) </b> </td>

</tr>

<tr> 

<td> EPI {
<p> *** id: number (8), 
<p> * status: string (1), // A = Ativo |I = Inativo
<p> * descricao: string (60),
<p> codigoCA: string(2),
<p> **dataValidadeCA: date,
<p> * Categoria: string (2),
<p> * Classe: string (2)
<p> }
<p> <b> Opções </b>
<p> <b> status: </b>
<p> A = Ativo
<p> I = Inativo
<p> <b> codigoCA </b>
<p> Informar o código da categoria do EPI, verificar a lista de opções na sessão de glossário. LISTA
<p> <b> Classe </b>
<p> Informar o código da classe do EPI, verificar a lista de opções na sessão de glossário. LISTA
<p> <b> * </b> Obrigatório
<p> <b> ** </b> Obrigatório caso o codigoCA seja preenchido.
<p> <b> *** </b>  Obrigatório em caso de edição (PUT)

</td>

</tr>

</table>

<br>

<table>

<tr>

<td> <b> EPI V2 </b> </td>
</tr>
<tr> 

<td> EPI  V2 {
<p> id: number (8), 
<p> status: string (1),
<p> codigo: string (20),,
<p> descricaoPT: string (2000),,
<p> descricaoEN: string (2000),
<p> descricaoES: string (2000),
<p> codigoCA: string (10),
<p> validadeCA: date
<p> }
<p> 
<p> <b> OBS: Caso nao seja informado valores para os atributos descricaoEN e descricaoES, o sistema automaticamente irá copiar as informações do atributo descricaoPT. </b>

</td>
</tr>
</table>

<center> <h3> [Início] (/manual-de-integração/modelo-de-dados/modelo-de-dados-1/) <h3> </center>

<center> <h3> <b> [Sumário] (/manual-de-integração/) </b> </center>
