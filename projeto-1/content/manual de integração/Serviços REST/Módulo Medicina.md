+++
title = "3. Módulo Medicina"
date =  2019-02-11T14:08:44-02:00
weight = 4
+++

## Cadastro Profissionais Medicina

### *Listar Profissionais Medicina* ---------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /si/cadastro/profissional/{status}/{orgao} </b></td>   
</tr>
   
<tr>
<td> <b> Exemplos: </b> 
<p> /si/cadastro/profissional/A/1
<p> /si/cadastro/profissional/A/1,3
<p> /si/cadastro/profissional/A,I/1,3
<p> <b> Descrição: </b>
<p> Este serviço permite os clientes listar todos os Profissionais cadastrados no Apollus. Útil para recuperar os códigos internos utilizados em outros serviços: Ex: Cadastro afastamento.
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
<td> A = Ativo
<p> I = Inativo
<p> T = Todos
</td>
</tr>

<tr>
<td> {orgao} </td> 
<td> 1 = CRM
<p> 2 = CRS
<p> 3 = CRO
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
<td> Array de Profissional
[Schema Profissional]

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

## Cadastro Grupo Risco

### *Lista Grupo de Risco* --------------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /si/cadastro/grupos_riscos</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite os clientes listar todos os Grupos de Riscos cadastrados no Apollus. 
</td>
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
<td> Array de Grupo Risco
[Schema Grupo Risco]


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

### *Criar Grupo de Risco* ----------------------------------

<br>

<table border="1">

<tr>
<td><b> POST /si/cadastro/grupo_risco</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
Este serviço permite os clientes cadastrar um Grupo de Risco no Apollus. 
<p> <b> OBS: </b>  Este serviço também permite vincular pessoas, contudo antes de realizar os vinculo o Sistema Apollus apaga todos os vínculos existentes no momento. Assim tomar muito cuidado com os dados inseridos manualmente via Sistema WEB
<p> <b> OBS: </b> Caso o usuário não informe nada no atributo PESSOAS, o serviço não ira apagar os vínculos já existente.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Afastamento </td> 
<td> Objeto Grupo Risco
[Schema Grupo Risco] </td>
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
<td> Verifica resposta no glossário.</td> 
</td>
</tr>

</table> 

<br>

<br>

### *Atualizar Grupo de Risco* ------------------------------------

<br>

<table border="1">

<tr>
<td><b> PUT /si/cadastro/grupo_risco</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite os clientes atualizar um Grupo de Risco no Apollus. 
<p> <b> OBS: </b> Este serviço também permite vincular pessoas, contudo antes de realizar os vinculo o Sistema Apollus apaga todos os vínculos existentes no momento. Assim tomar muito cuidado com os dados inseridos manualmente via Sistema WEB
<p> <b> OBS: </b> Caso o usuário não informe nada no atributo PESSOAS, o serviço não ira apagar os vínculos já existente.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Afastamento</td> 
<td> 
Objeto Grupo Risco
[Schema Grupo Risco]

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

## Prontuário

### *Listar CAT por funcionário* --------------------------

<br>

<table border="1">

<tr>
<td><b>GET /si/prontuario/cat/pessoa/{id_funcionario}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite que os clientes listem as CATs de um determinado funcionário cadastrado no Apollus. Útil para recuperar os códigos internos utilizados em outros serviços: Ex: Cadastro afastamento.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {id_funcionario} </td> 
<td> Código Interno do Apollus referente a uma pessoa.

</td>
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
<td> 200</td> 
<td> Sucesso</td>
<td> Array de CAT
[Schema CAT]
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


### *Criar Afastamento* --------------------------

<br>

<table border="1">

<tr>
<td><b>POST /si/prontuário/afastamento</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite ao cliente criar um registro de Afastamento dentro do Sistema Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Afastamento
</td> 
<td> Objeto Afastamento
[Schema Afastamento]
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

# *Propriedades de Requisição*

<br>

<table border="1">

<tr>
<td> <b> Propriedade</b></td> 
<td> <b> Descrição</b> </td>
<td> <b> Tipo</b> </td>
<td> <b> Tamanho</b> </td>
<td> <b> Obrigatório</b> </td>
</tr>
   
<tr>
<td> codigoFuncionario </td>
<td> Código interno do funcionário dentro do Apollus. 
<p> Utilizar o serviço de Listar Pessoa para recuperação do código interno. </td>
<td> Numérico </td>
<td> 20 </td>
<td> Sim </td>
</tr>

<tr>
<td> codigoResponsavelRegistro </td>
<td> Código interno da pessoa que será o responsável pelo registro do Afastamento. </td>
<td> Numérico </td>
<td> 20 </td>
<td> Sim </td>
</tr>

<tr>
<td> inicioAfastamento </td>
<td> Data que iniciou o afastamento. </td>
<td> Texto (dd/MM/yyyy) </td>
<td> 10 </td>
<td> Sim </td>
</tr>

<tr>
<td> totalDiasAfastado </td>
<td> Total de dias para afastamento. </td>
<td> Numérico </td>
<td> 3 </td>
<td> Sim </td>
</tr>

<tr>
<td> dataRetorno </td>
<td> Data de retorno do funcionário </td>
<td> Texto (dd/MM/yyyy) </td>
<td> 10 </td>
<td> Não </td>
</tr>

<tr>
<td> motivoAfastamento </td>
<td> 01 = Acidente/Doença do trabalho. </td>
<td> Texto </td>
<td> 2 </td>
<td> Sim </td>
</tr>

<tr>
<td>  </td>
<td> 01 = Acidente/Doença do trabalho.
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
<p> 32 - Transferência para prestação de serviços no exterior em período superior a 90 dias'
</td>
<td>  </td>
<td>  </td>
<td>  </td>
</tr>


<tr>
<td> numeroCAT </td>
<td> Código Interno do Apollus. 
<p> Utilizar o serviço Buscar CAT para recuperar o código interno;
 </td>
<td> Numérico </td>
<td> 20</td>
<td> SIM, quando o campo motivoAfastamento for preenchido com a opção “01” </td>
</tr>

<tr>
<td> mesmoMotivo </td>
<td> S = SIM
<p> N = NÃO
 </td>
<td> Texto </td>
<td> 1 </td>
<td> Sim </td>
</tr>

<tr>
<td> tipoAcidenteTransito </td>
<td> 1 = Atropelamento
<p> 2 = Colisão
<p> 3 = Outros
 </td>
<td> Número </td>
<td> 1 </td>
<td> Não </td>
</tr>

<tr>  
<td> horaSaida</td>
<td> </td>
<td> Texto (00:00) </td>
<td> 5 </td>
<td> Não </td>
</tr>

<tr>  
<td> horaRetorno </td>
<td> </td>
<td> Texto (00:00) </td>
<td> 5 </td>
<td> Não</td>
</tr>

<tr>  
<td> maior15Dias </td>
<td> Flag </td>
<td> Booleano </td>
<td> - </td>
<td> Não</td>
</tr>

<tr>  
<td> afastamentoDefinitivo </td>
<td> Flag </td>
<td> Booleano </td>
<td> - </td>
<td> Não </td>
</tr>

<tr>  
<td> observacoes </td>
<td> </td>
<td> Texto </td>
<td> 400 </td>
<td> Não </td>
</tr>

<tr>  
<td> codigoCid </td>
<td> Codigo do CID </td>
<td> Texto </td>
<td> 60 </td>
<td> Sim </td>
</tr>

<tr>  
<td> descricaoCid </td>
<td> </td>
<td> Texto </td>
<td> 60 </td>
<td> Sim </td>
</tr>

<tr>  
<td> codigoClassificacaoInterna </td>
<td> Código interno do Apollus.
<p> Utilizar o serviço Buscar Classificação Interna para recuperar os códigos internos; </td>
<td> Numérico </td>
<td> 20 </td>
<td> Não </td>
</tr>

<tr>  
<td> atestadoExterno </td>
<td> </td>
<td> Booleano</td>
<td> - </td>
<td> Não </td>
</tr>

<tr>  
<td> alerta </td>
<td> </td>
<td> Booleano</td>
<td> - </td>
<td> Não </td>
</tr>

<tr>  
<td> codigoUnidadeAtendimento </td>
<td> Código Interno do Apollus.
<p> Utilizar o serviço Buscar Centro Medico para recuperar os códigos interno. </td>
<td> Numérico </td>
<td> 20 </td>
<td> SIM - Caso a FLAG “atestadoExterno” NÃO esteja marcada. </td>
</tr>

<tr>  
<td> codigoProfissional </td>
<td> Código Interno do Apollus. 
<p> Utilizar o serviço Buscar Profissional Medicina para recuperar os códigos interno. </td>
<td> Numérico </td>
<td> 20 </td>
<td> SIM - Caso a FLAG “atestadoExterno” NÃO esteja marcada. </td>
</tr>

<tr>  
<td> nomeUnidadeAtendimento </td>
<td> Nome/Descrição da unidade externa que realizou o afastamento. </td>
<td> Texto </td>
<td> 80 </td>
<td> SIM - Caso a FLAG “atestadoExterno” esteja marcada. </td>
</tr>

<tr>  
<td> cidadeUnidadeAtendimento </td>
<td>  </td>
<td> Texto </td>
<td> 80 </td>
<td> SIM - Caso a FLAG “atestadoExterno” esteja marcada. </td>
</tr>

<tr>  
<td> profissionalExterno </td>
<td> Nome do profissional. </td>
<td> Texto </td>
<td> 80 </td>
<td> SIM - Caso a FLAG “atestadoExterno” esteja marcada. </td>
</tr>

<tr>  
<td> orgaoProfissionalExterno </td>
<td> Orgao do profissional.
<p> 1 = CRM
<p> 2 = RMS
<p> 3 = CRO </td>
<td>  </td>
<td> 1 </td>
<td> SIM - Caso a FLAG “atestadoExterno” esteja marcada. </td>
</tr>

<tr>  
<td> ufOrgaoProfissionalExterno </td>
<td> Sigla </td>
<td> Texto </td>
<td> 2 </td>
<td> SIM - Caso a FLAG “atestadoExterno” esteja marcada. </td>
</tr>

<tr>  
<td> inscricaoProfissionalExterno </td>
<td> Número da incrição </td>
<td> Numérico </td>
<td> 14 </td>
<td> SIM - Caso a FLAG “atestadoExterno” esteja marcada. </td>
</tr>

</table>

# *Requisição JSON*


    { “codigoFuncionario”: 1, 
     “codigoResponsavelRegistro”: 1,
     “inicioAfastamento”: “00/00/0000”,
     “totalDiasAfastado”: 000,
     “dataRetorno”: “00/00/0000”,
     “motivoAfastamento”: “01”,
     “numeroCat”: 1,
     “mesmoMotivo”: “S”,
     “tipoAcidenteTransito”: 1,
     “horaSaida”: “00:00”,
     “horaRetorno”: “00:00”,
     “maior15Dias”: true,
     “afastamentoDefinitivo”: false,
     “observacoes”: “loren ypson”,
     “codigoCid”: “M010”,
     “codigoClassificacaoInterna”: 1,
     “atestadoExterno”: false,
     “alerta”: true,
     “codigoUnidadeAtendimento”: 1,
     “codigoProfissional”: 1,
     “nomeUnidadeAtendimento”: “loren ypson”,
     “cidadeUnidadeAtendimento”: “loren ypson”,
     “profissionalExterno”: “loren ypson”,
     “orgaoProfissionalExterno”: 1
     “ufOrgaoProfissionalExterno”: “loren ypson”,
     “inscricaoProfissionalExterno” : 1
     }
	 
# Propriedades do Retorno:

<table>

<tr> 
<td> <b> Propriedade </b> </td>
<td> <b> Descrição </b> </td>
<td> <b> Tipo </b> </td>
<td> <b> Tamanho </b> </td>
 </tr>
 
 <tr> 
<td> codigoApollus  </td>
<td> Código Interno Apollus </td>
<td> Numérico </td>
<td> 20 </td>
 </tr>
 
 <tr> 
<td> numeroServico </td>
<td> Número do serviço gerado </td>
<td> Texto </td>
<td> 20 </td>
 </tr>
 
</table>

<br>

# Retorno formato JSON:

    {
    “code”: 0,
    “message”: “OK”,
    “data”: [
        {
    “codigoApollus”: 1,
    “numeroServico”: “000000000”
        }
    ]
    }
	

### *Atualizar Afastamento* ---------------------------------

<br>

<table border="1">

<tr>
<td><b> PUT /si/prontuário/afastamento</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b>
<p> Este serviço permite ao cliente atualizar um registro de Afastamento dentro do Sistema Apollus.
<p> Atentar na atualização de um afastamento, pois existem 3 campos extras a serem preenchidos.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Afastamento </td> 
<td>Objeto Afastamento
[Schema Afastamento]

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

### *Listar Afastamentos* --------------------------------------

<br>

<table border="1">

<tr>
<td><b>GET /si/prontuario/afastamento/pessoa/{id_funcionario}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a leitura dos Afastamentos de um determinado funcionário cadastrado no Apollus.
</td>
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
<td> Array de Afastamento
[Schema Afastamento]


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

### *Listar Afastamento Período* ----------------------------------

<br>

<table border="1">

<tr>
<td><b> GET /si/prontuario/afastamento/periodo_registro/{dataInicio}/{dataFim}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
Este serviço permite a leitura dos Afastamentos cadastrados em um determinado período.
O período informado não pode ultrapassar a 10 dias.

</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {dataInicio }  </td> 
<td> Informar no padrão: yyyy-MM-dd </td>
</tr>

<tr>
<td> {dataFim}  </td> 
<td> Informar no padrão: yyyy-MM-dd </td>
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
<td> Array de Afastamento
[Schema Afastamento]



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

### *Criar ASO* ------------------------------------

<br>

<table border="1">

<tr>
<td><b> POST /si/prontuário/afastamento</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite ao cliente criar um registro de ASO dentro do Sistema Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Afastamento</td> 
<td> Objeto ASO
[Schema ASO]

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

### *Atualizar ASO* --------------------------

<br>

<table border="1">

<tr>
<td><b>PUT /si/prontuário/aso</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite ao cliente atualizar um registro de ASO dentro do Sistema Apollus.
</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> Afastamento </td> 
<td> Objeto ASO
[Schema ASO]

</td>
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


### *Listar ASO Período* --------------------------

<br>

<table border="1">

<tr>
<td><b>GET /si/prontuario/aso/periodo_registro/{dataInicio}/{dataFim}</b></td>   
</tr>
   
<tr>
<td> <b> Descrição: </b> 
<p> Este serviço permite a leitura dos ASOS cadastrados em um determinado período.
O período informado não pode ultrapassar a 10 dias.

</td>
</table>

#### Parâmetros:
 
<table>

<tr>
<td> <b>Parâmetro </b></td> 
<td> <b>Descrição </b>  </td>
</tr>

<tr>
<td> {dataInicio } 
</td> 
<td> Informar no padrão: yyyy-MM-dd
</td>
</tr>

<tr>
<td> {dataFim} 
</td> 
<td> Informar no padrão: yyyy-MM-dd
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
id: Array de ASO
[Schema ASO]
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

<center> <h3> [Início] (/manual-de-integração/serviços-rest/módulo-medicina/) <h3> </center>

<center> <h3> <b> [Sumário] (/manual-de-integração/) </b> </center>





