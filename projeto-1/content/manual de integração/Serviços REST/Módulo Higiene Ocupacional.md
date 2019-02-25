+++
title = "Módulo Higiene Ocupacional"
date =  2019-02-11T14:08:44-02:00
weight = 3

+++

#### **GHE**

#### *Listar GHEs por Status* ---------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /hoe/ghe/status/{status} </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite que os clientes listem os dados de todos os GHEs cadastrados no Apollus filtrando pelo status.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {status} </td> 
<td> Status disponíveis.
<p> A = Ativo
<p> I = Inativo
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (code) </b> </td> 
<td> <b>Descrição (message) </b> </td>
<td> <b>Schema <b/> </td>
</tr>

<tr>
<td> 200 </td> 
<td> Sucesso </td>
<td> Array de GHE
[Schema GHE]
 </td>
</tr>
  
</table>

#### Erro:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
</tr>

<tr>
<td> XX </td> 
<td> Verifica resposta no glossário.</td> 
</td>
</tr>

</table>

<br>

<br>

#### *Listar GHEs por Área* --------------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /hoe/ghe/area/{id_area}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite que os clientes listem os dados de todos os GHEs vinculados a uma determinada área cadastrada no Apollus. Este serviço é útil para recuperar os códigos internos utilizados em outros serviços: Ex: Cadastro de uma pessoa (funcionário).
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id_area} </td> 
<td> Código interno do Apollus referente a uma Área nivel 1 
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b> Schema <b/> </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> Array de GHE
[Schema GHE]

</td>
</tr>

  
</table>

#### Erro:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
</tr>

<tr>
<td> XX </td> 
<td> Verifica resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

#### *Detalhar GHE por ID* ----------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /hoe/ghe/{id_ghe}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
Este serviço detalha um GHE com todos os dados.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id_ghe} </td> 
<td> Código interno do Apollus referente a uma GHE </td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b> </td>
<td> <b>Schema </b> </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> Array de GHE
[Schema GHE]

</td>
</tr>

  
</table>

#### Erro:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
</tr>

<tr>
<td> XX </td> 
<td> Verifica resposta no glossário.</td> 
</td>
</tr>

</table> 

<br>

<br>

#### *Criar GHE* ------------------------------------

<br>

<table border="1">

<tr>
<td><b> POST /hoe/ghe</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a atualização dos dados de uma pessoa (funcionário) dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> GHE</td> 
<td> 
Objeto GHE
[Schema GHE]

</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b> Schema </b> </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> {
id: << identificador gerado >>
}
 </td>

</tr>

  
</table>

#### Erro:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
</tr>

<tr>
<td> XX </td> 
<td> Verifica resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

#### *Atualizar GHE* --------------------------

<br>

<table border="1">

<tr>
<td><b>PUT /hoe/ghe</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a atualização de um GHE dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> GHE</td> 
<td> Objeto GHE
[Schema GHE]

</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>

</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>

</tr>

  
</table>

#### Erro:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
</tr>

<tr>
<td> XX </td> 
<td> Verifica resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>


#### *Listar Cálculos Estatístico por GHE* --------------------------

<br>

<table border="1">

<tr>
<td><b>GET /hoe/ghe/listar_calculos_estatisticos/{id_ghe}/{data_base}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite que os clientes listem todos os cálculos estatísticos de um determinado GHE.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id_ghe} 
</td> 
<td> Codigo interno do apollus que identifica um GHE
</td>
</tr>

<tr>
<td> {data_base} 
</td> 
<td> Data de referencia dentro de um Periodo
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b> Schema </b> </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> Cálculos
[Schema CalculoEstatisticoGHE] </td>
</tr>

  
</table>

#### Erro:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
</tr>

<tr>
<td> XX </td> 
<td> Verifica resposta no glossário.</td> 
</td>
</tr>

</table>

<br>

<center> <h3> [Início] (/manual-de-integração/serviços-rest/módulo-higiene-ocupacional/) <h3> </center>



 
  
 