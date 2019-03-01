+++
title = "1. Módulo Cadastro"
date =  2019-02-11T14:08:44-02:00
weight = 2
+++

## Áreas (Estrutura)

### *Lista Áreas* -----

<br>

<table border="1">

<tr>
<td><b> GET /cadastro/area/{id_area} </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite que os clientes listem os dados de todas as áreas cadastradas no Apollus, filtrando pelo ID  da Área.
<p> Deve ser informado na requisição o ID da Área de nível 1 , 2 ou 3.
<p> Informando o ID de uma Área nível 1 o serviço retorna todos os dados da área 1 e suas filhas.
<p> Informando o ID de uma Área nível 2 o serviço retorna todos os dados da área 2 e suas filhas.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> id_area </td> 
<td> Código que identifica uma Área dentro do Apollus.
Este ID deve ser referente a uma Área.</td> 
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema </b>  </td>
</tr>

<tr>
<td> 200 </td> 
<td> Sucesso</td> 
<td> Array de áreas.
[Schema Area]
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>
  
</table>

<br>

<br>


### *Listar Todas Áreas nível 1* -----

<br>

<table border="1">

<tr>
<td><b> GET /cadastro/area/areas_nivel_1 </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite que os clientes listem os dados de todas as áreas de nível 1 cadastradas no Apollus.
</td>
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Codigo (code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema </b>  </td>
</tr>

<tr>
<td> 200 </td> 
<td> Sucesso</td>
<td> Array de Areas.
[Schema Area]
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>

<br>

<br>

### *Inativar Áreas* -----

<br>

<table border="1">

<tr>
<td><b> PUT  /cadastro/area/inativar/{id}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite que os clientes inativem uma determinada Área. 
</td>
</table>

#### <b>  Parâmetros </b>:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id}</td> 
<td> Código interno do Apollus que identifica uma determinada Área.</td>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Criar Área* -----

<br>

<table border="1">

<tr>
<td><b> POST  /cadastro/area</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a criação de uma Área dentro do Apollus.  
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Área</td> 
<td> Objeto Area
 [Schema Area]</td>
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
<td> {
id: << identificador >>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table> 

<br>

<br>

### *Atualizar Áreas* -----

<br>

<table border="1">

<tr>
<td><b> PUT  /cadastro/area </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a atualização de uma Área dentro do Apollus. 
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Área</td> 
<td> Objeto Area
 [Schema Area]</td>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Excluir Áreas* -----

<br>

<table border="1">

<tr>
<td><b> DELETE  /cadastro/area/{id_area_pai}/{id_area_filha}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a exclusão de uma Área dentro do Apollus. Desde que a área a ser excluída seja de nível 2 ou 3.
<p> Área de nível 1 apenas a Apollus pode excluir. 
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id_area_pai}</td> 
<td> Código Interno do Apollus, este é o código da Área Pai na qual a Área a ser excluída é uma filha.</td>
</tr>

<tr>
<td> {id_area_filha}</td> 
<td> Código Interno do Apollus, este é o código da Área que será <b> excluida <b>.</td>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>
 
## Cargo

### *Listar Cargos pelo Status* --------------------------

<br>

<table border="1">

<tr>
<td><b> GET /cadastro/cargo/{status} </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite listar todos os cargos cadastrados no Apollus. Filtrando pelo campo “STATUS”
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Status </td> 
<td> Status disponíveis.
<p> A = Ativo
<p> I = Inativo
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema </b> </td>
</tr>

<tr>
<td> 200 </td> 
<td> Sucesso </td> 
<td> Array de Cargos.
Schema Cargo </td> 
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>

<br>

<br>

### *Criar Cargo* --------------------------------------

<br>

<table border="1">

<tr>
<td><b> POST /cadastro/cargo</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a criação de um Cargo dentro do Apollus.
</td>
</table>

#### <b> Parâmetros  </b>:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Cargo</td> 
<td> Objeto Cargo
 [Schema Cargo] </td>
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
<td> {
Id: << identificador gerado >>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Atualizar Cargo* ----------------------------------

<br>

<table border="1">

<tr>
<td><b> PUT  /cadastro/cargo</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a criação de um Cargo dentro do Apollus.  
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Cargo</td> 
<td> Objeto Cargo
 [Schema Area]</td>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table> 

<br>

<br>

### *Excluir Cargo* ------------------------------------

<br>

<table border="1">

<tr>
<td><b> DELETE  /cadastro/cargo/{id}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a exclusão de um Cargo dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id}</td> 
<td> Código interno que Identifica um cargo dentro do Apollus.</td>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

## Centro Custo

### *Listar Centros de Custo* --------------------------

<br>

<table border="1">

<tr>
<td><b>GET /cadastro/centro_custo/{status}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite listar todos os Centro de Custos cadastrados no Apollus. Filtrando pelo campo “STATUS”
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Status</td> 
<td> Status disponíveis.
<p> A = Ativo
<p> I = Inativo
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> Array de Centro de Custo.
[Schema CentroCusto]
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Criar Centro Custo* -------------------------------

<br>

<table border="1">

<tr>
<td><b>POST  /cadastro/centro_custo</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a criação de um Centro de Custo dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> CentroCusto</td> 
<td> Objeto CentroCusto
 [Schema CentroCusto]</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> {
Id: << identificador gerado >>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Atualizar Centro Custo* ---------------------------

<br>

<table border="1">

<tr>
<td><b>POST  /cadastro/centro_custo</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a atualização de um Centro de Custo dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> CentroCusto</td> 
<td> Objeto CentroCusto
 [Schema CentroCusto]
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Excluir Centro Custo* -----------------------------

<br>

<table border="1">

<tr>
<td><b>DELETE  /cadastro/centro_custo/{id}</td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a exclusão de um Centro de Custo dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id}</td> 
<td> Código interno que Identifica um centro de custo dentro do Apollus.
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>


## EPI

### *Listar EPIs* ---------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /cadastro/epi/{status} </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite listar todos os EPIs cadastrados no Apollus. Filtrando pelo campo “STATUS”
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Status </td> 
<td> Status disponíveis.
<p> A = Ativo
<p> I = Inativo
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema </b> </td>
</tr>

<tr>
<td> 200 </td> 
<td> Sucesso </td> 
<td> Array de EPI
[Schema EPI]
 </td> 
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>

<br>

<br>

### *Criar EPI* --------------------------------------

<br>

<table border="1">

<tr>
<td><b> POST  /cadastro/epi</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a criação de um EPI dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> EPI</td> 
<td> Objeto EPI
 [Schema EPI] </td>
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
<td> {
Id: << identificador gerado >>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Atualizar EPI* ----------------------------------

<br>

<table border="1">

<tr>
<td><b> POST  /cadastro/epi</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a criação de um EPI dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> EPI</td> 
<td> Objeto EPI
 [Schema EPI]</td>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table> 

<br>

<br>

### *Excluir EPI* ------------------------------------

<br>

<table border="1">

<tr>
<td><b> DELETE  /cadastro/epi/{id}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a exclusão de um EPI dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id}</td> 
<td> 
Código interno que Identifica um EPI dentro do Apollus.
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

## EPI V2 - Nova Versão do EPI

### *Criar EPI V2* --------------------------

<br>

<table border="1">

<tr>
<td><b>POST  / equipamento /epi</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a criação de um EPI na V2 dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> EPI</td> 
<td> Objeto EPI
 [Schema EPI V2]
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> {
Id: << identificador gerado >>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
  <h5> OBS: Caso nao seja informado valores para os atributos descricaoEN e descricaoES, o sistema automaticamente irá copiar as informações do atributo descricaoPT.</h5>
  
<br>

<br>


### *Excluir EPI V2* --------------------------

<br>

<table border="1">

<tr>
<td><b>DELETE  /equipamento/epi/{id}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a exclusão de um EPI dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id}</td> 
<td> Código interno que Identifica um EPI dentro do Apollus.
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
  
<br>

<br>

### *Listar Epis Por Código CA e Período Edição* -------------

<br>

<table border="1">

<tr>
<td><b>GET /equipamento/epi/listar_pelo_ca_periodo_edicao/{ca}/{inicio}/{fim}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a leitura dos EPIs V2 cadastradas no Apollus. 
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> { ca } </td> 
<td> Código do CA a ser filtrado. 
</td>
</tr>

<tr>
<td> {inicio}</td> 
<td> Período inicial da última edição.
</td>
</tr>

<tr>
<td> {fim}</td> 
<td> Período final da última edição.
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> Array de EPI V2
[Schema Epi V2]

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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
  
<br>

<br>

### *Listar Epis Por Código e Período Edição* ----------

<br>

<table border="1">

<tr>
<td><b>GET /equipamento/epi/listar_pelo_codigo_periodo_edicao/{codigo}/{inicio}/{fim} </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a leitura dos EPIs V2 cadastradas no Apollus. 
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> { codigo }  </td> 
<td> Código do EPI a ser filtrado.  
</td>
</tr>

<tr>
<td> {inicio}</td> 
<td> Período inicial da última edição.
</td>
</tr>

<tr>
<td> {fim}</td> 
<td> Período final da última edição.
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> Array de EPI V2
[Schema Epi V2]

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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>


## Pessoas

### *Listar Líderes* ---------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /cadastro/pessoa/lideres </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a leitura dos Ids (códigos internos) das Pessoas cadastradas como Lideres no Apollus. 
</td>
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
<td> Array de PessoaLider
[Schema PessoaLider]
 </td>
</tr>
  
</table>

<td> 200 </td> 
<td> Sucesso </td> 
<td> Array de EPI
[Schema EPI]
 </td> 
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>

<br>

<br>

### *Listar Pessoas (Matricula + CPF + Nome)* --------------------

<br>

<table border="1">

<tr>
<td><b> GET /cadastro/pessoa/matricula_cpf_nome/{tipo_pesquisa}/{valor_pesquisa}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a leitura dos códigos internos das Pessoas cadastradas no Apollus aplicando filtro por: Matricula, CPF ou Nome.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> { tipo_pesquisa } </td> 
<td> Informa ao serviço qual parâmetro de busca o sistema deve utilizar;
<p> - Opções: 
<p> M = busca por matricula. Deve ser informada uma matricula completa; 
<p> C = busca por cpf. Deve ser informado um CPF completo;
<p> N = busca por nome. Pode informar parte do nome; Mínimo 3 letras para efetuar a busca.
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
<td> Array de Pessoa
[Schema Pessoa]

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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Criar Pessoa* ----------------------------------

<br>

<table border="1">

<tr>
<td><b> POST  /cadastro/pessoa</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a criação de uma pessoa (funcionário) dentro do Apollus.
<p> <b> Observação 1: </b> Ao criar a pessoa e passar o valor “true” no campo “limparHistorico”, caso haja algum PPP para este funcionário, os dados de profissiografia serão limpos e não será possível recuperar. 
<p> <b> Observação 2: </b> Ao criar uma pessoa não é possível informar ZERO ‘0’ na propriedade GHE a qual possibilita o mecanismo de sincronização aplicada no PUT.
</td>
</table>

#### <b> Parâmetros  </b>:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Pessoa</td> 
<td> Objeto Pessoa
 [Schema Pessoa]</td>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table> 

<br>

<br>

### *Atualizar Pessoa* ------------------------------------

<br>

<table border="1">

<tr>
<td><b> PUT  /cadastro/pessoa</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a atualização dos dados de uma pessoa (funcionário) dentro do Apollus.
<p> <b> Observação: </b> Ao criar a pessoa e passar o valor “true” no campo “limparHistorico”, caso haja algum PPP para este funcionário, os dados de profissiografia serão limpos e não será possível recuperar. 
</td>
</table>

#### <b> Parâmetros  </b>:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Pessoa</td> 
<td> 
Objeto Pessoa
 [Schema Pessoa]
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>

### *Exclui pessoa* --------------------------

<br>

<table border="1">

<tr>
<td><b>DELETE  /cadastro/pessoa/{id}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a exclusão de uma Pessoa dentro do Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id}</td> 
<td> Código interno que Identifica uma Pessoa dentro do Apollus.
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<br>


### *Inativar Pessoa* --------------------------

<br>

<table border="1">

<tr>
<td><b>PUT  /cadastro/pessoa/inativar_pessoa</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a inativação de uma Pessoa dentro do Apollus.
<p> Ações:
<p> - Alterar status para Inativo
<p> - Limpar campo email.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {
“matricula” : {matricula/id}
}
</td> 
<td> Código interno que Identifica uma Pessoa dentro do Apollus.
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
  
<br>

<br>

### *Listar Riscos* --------------------------

<br>

<table border="1">

<tr>
<td><b>GET /cadastro/risco/risco_simples</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a leitura de todos os riscos cadastrados no Apollus.
</td>
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> Array de Risco
[Schema Risco]

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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
  
<br>

<br>

## Turno


### *Listar Turnos Pela Area 1* --------------------------

<br>

<table border="1">

<tr>
<td><b>GET /cadastro/turno/listar_turnos_pela_area_1 </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a leitura de todos os turnos cadastrados no Apollus filtrando pelos turnos vinculados nas Áreas de nível 1.
</td>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> Array de Turno
[Schema Turno]

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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
  
<br>

<br>

### *Criar Turno* --------------------------

<br>

<table border="1">

<tr>
<td><b>POST  /cadastro/turno </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a criação de um Turno dentro do Apollus.
</td>
  
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Turno </td> 
<td> Objeto Turno
 [Schema Turno]
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> {
Id: << identificador gerado >>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
  
<br>

<br>

### *Atualizar Turno* --------------------------

<br>

<table border="1">

<tr>
<td><b>POST  /cadastro/turno </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a criação de um Turno dentro do Apollus.
</td>
  
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> EPI </td> 
<td> Objeto Turno
 [Schema TURNO]
</td>
</tr>
  
</table>

#### Resposta:
 
<table>

<tr>
<td> <b>Código (Code) </b></td> 
<td> <b>Descrição (message) </b>  </td>
<td> <b>Schema</b>  </td>
</tr>

<tr>
<td> 200</td> 
<td> Sucesso</td>
<td> {
Id: << identificador gerado >>
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
  
<br>

<br>

### *Excluir Turno* --------------------------

<br>

<table border="1">

<tr>
<td><b>DELETE  /cadastro/turno/{id} </b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Permite a exclusão de um Turno dentro do Apollus.
</td>
  
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id} </td> 
<td> Código interno que Identifica um Turno dentro do Apollus.
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
<td> Verifica Resposta no glossário.</td> 
</td>
</tr>

</table>
  
<br>

<center> <h3> [Início] (/manual-de-integração/serviços-rest/módulo-cadastro/) <h3> </center>

<center> <h3> <b> [Sumário] (/manual-de-integração/) </b> </center>


  