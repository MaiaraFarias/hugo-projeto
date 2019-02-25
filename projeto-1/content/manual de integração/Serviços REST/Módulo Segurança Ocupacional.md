+++
title = "Módulo Segurança Ocupacional"
date =  2019-02-11T14:08:44-02:00
weight = 5
+++

#### **Gestão Epi**

#### *Listar Epi ESocial* ---------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /so/gestão_epi/listar_epi_esocial_pessoa/{matricula}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b>
<p> Permite a leitura de todos os EPIs associados a um Risco vinculados para um determinado Funcionário. 

<p> Este serviço é útil aos clientes que não utilizam o modulo Gestão EPI do Apollus, mas que necessitam desta informação para o envio do eSocial.

</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {matricula}  </td> 
<td>Código interno do Apollus que identifica uma pessoa

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
<td> Array de EpiESocial
[Schema EpiESocial]


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

#### *Criar Epi ESocial* --------------------------------------

<br>

<table border="1">

<tr>
<td><b>POST  /so/gestão_epi/epi_esocial</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite criar um EPI associado a um Risco vinculados para um determinado Funcionário. 
<p> Este serviço é útil aos clientes que não utilizam o modulo Gestão EPI do Apollus, mas que necessitam desta informação para o envio do eSocial.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> EpiESocial  </td> 
<td>Objeto EpiESocial
 [Schema EpiEsocial]

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

#### *Atualizar Epi ESocial* ----------------------------------

<br>

<table border="1">

<tr>
<td><b> PUT  /so/gestão_epi/epi_esocial</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
Permite atualizar um EPI associado a um Risco vinculados para um determinado Funcionário. 
<p> Este serviço é útil aos clientes que não utilizam o modulo Gestão EPI do Apollus, mas que necessitam desta informação para o envio do eSocial.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> EpiESocial  </td> 
<td> Objeto EpiESocial
 [Schema EpiEsocial] </td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b> </td>

</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>

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

<center> <h3> [Início] (/manual-de-integração/serviços-rest/módulo-segurança-ocupacional/) <h3> </center>
