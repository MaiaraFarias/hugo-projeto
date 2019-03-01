+++
title = "7. Glossário"
date =  2019-02-11T14:08:44-02:00
weight = 7
+++

#### **Token**: é um código de segurança também conhecido como chave de produção e key data. Todo o cliente precisa possuir esse token para conseguir consumir os serviços do Apollus.

#### Códigos retornados em caso de erro, identificando o motivo do erro e suas respectivas mensagens.

<br>

<table border="1">
   <tr>
   <td><b> CÓDIGO </b></td> 
   <td><b> MENSAGEM</b></td> 
   <td><b> DESCRIÇÃO</b></td> 
   </tr>
   
   <tr>
   <td>  0</td> 
   <td>  Sucesso </td> 
   <td>  Requisição processada com sucesso.</td> 
   </tr>
  
   <tr>
   <td>  50</td> 
   <td>  Token inválido. </td>
   <td>  O token informado na requisição possui alguma irregularidade.</td>
   </tr>
   
    <tr>
   <td>  51</td> 
   <td>  Token inexistente. </td>
   <td>  Não foi informado um token na requisição.</td>
   </tr>
   
    <tr>
   <td>  52</td> 
   <td>  Token desativado. </td>
   <td>  O Token informado foi desativado. Favor entrar em contato o suporte.</td>
   </tr>
   
    <tr>
   <td>  53</td> 
   <td> Valor do campo ({0}) informado não corresponde ao esperado ({1}). </td>
   <td>  O valor informado para um determinado campo não segue as regras dos valores esperados.</td>
   </tr>
   
    <tr>
   <td>  54</td> 
   <td>  O campo {0} não foi preenchido. </td>
   <td>  O campo informado está vazio ou inválido.</td>
   </tr>
   
    <tr>
   <td>  55</td> 
   <td>  Campo ({0}) enviado excede o tamanho ({1}). </td>
   <td>  O tamanho do campo excede ao tamanho definido.</td>
   </tr>
   
    <tr>
   <td>  56</td> 
   <td>  O campo '{0}' não permite valores negativos ou zeros. </td>
   <td>  O valor do campo informado não pode ser negativo.</td>
   </tr>
   
    <tr>
   <td>  57</td> 
   <td>  O CNPJ informado é invalido. </td>
   <td>  O CNPJ informado é invalido. </td>
   </tr>
   
   <tr>
   <td>  58</td> 
   <td>  O campo {0} não esta sendo formatado corretamente. Formato esperado: {1} </td>
   <td>  O valor informado não aplica o padrão/mascara definido.</td>
   </tr>
   
   <tr>
   <td>  59</td> 
   <td>  A hora informada no campo ({0}) está inválida ({1}). </td>
   <td>  A hora informado esta fora do padrão. </td>
   </tr>
   
   <tr>
   <td>  60</td> 
   <td>  O formato do campo {0} informado está fora do padrão esperado. 10 ou 11 digitos. </td>
   <td>  O valor para telefone deve conter 10 ou 11 digitos.</td>
   </tr>
   
   <tr>
   <td>  61</td> 
   <td>  Favor informar o responsável pela edição. </td>
   <td>  Sempre que for realizado uma edição em prontuário é necessário informar um responsável da edição, assim como informado um responsável pelo Registro. </td>
   </tr>
   
   <tr>
   <td>  100</td> 
   <td>  Erro de Validação Geral.
- Mensagens personalizadas.
 </td>
   <td>  Gerado sempre que houve problemas de validação de regras de negocio no Sistema Apollus </td>
   </tr>
   
   </table>
   
   
## HTTP Status Code

#### Segue abaixo tabela de HTTP Status Code com algumas das respostas que podem ocorrer com mais frequência.

<br>

<table border="1">
   <tr>
   <td><b> HTTP STATUS </b></td> 
   <td><b> Code</b></td> 
   </tr>
   
   <tr>
   <td>  200</td> 
   <td>  OK – Tudo funcionou
   </tr>
   
   <tr>
   <td>  400</td> 
   <td>  Bad Request – Requisição inválida
   </tr>
   
   <tr>
   <td>  401</td> 
   <td>  Unauthorized  - Não autorizado
   </tr>
   
   <tr>
   <td>  404</td> 
   <td>  Resource Not Found – Não encontrado
   </tr>
   
   <tr>
   <td>  413</td> 
   <td>  Request is too large
   </tr>
   
   <tr>
   <td>  415</td> 
   <td>  Unsupported Media Type
   </tr>
   
   <tr>
   <td>  429</td> 
   <td>  Too Many Request – Quantidade solicitada excede o tamanho.
   </tr>
   
   <tr>
   <td>  500</td> 
   <td>  Internal Server Error
   </tr>
   
   </table>
   
<br>

## Estrutura JSON ERRO

#### Abaixo se encontra a estrutura (JSON) padrão de erro gerado pelo Apollus Integrador.
#### O JSON retorna uma lista de erros com seus devidos CODE e MESSAGE.
        {
               [
                        {
                               "code": 0,
                               "message": "OK"
                        }
               ]
        }  

<br>

## Definindo Atributos Vazios

#### Quando houver a necessidade em definir um atributo como vazio ou branco ou nulo deve-se usar o seguinte formato abaixo.

<br>

#### **Atributos simples**

#### String, Texto, Date, Number, Numerico.

    {
               nome:null
    }
	
#### **Atributos complexos**

#### Schemma/Objeto.

    {
               cargo:null
    }

## Definindo Atributo Data

#### Quando algum schemma fazer o uso do atributo DATE deve ser utilizado o padrão ISO8601;

    {
               data: ‘2000-12-25’
    }

## Definindo Atributos de Merge

#### Existe cenários onde o Consumidor dos serviços não possua uma informação que foi inserida manualmente dentro do Sistema Apollus. Deste modo é possível atualizar todo um Schema e mantendo essas informações previamente editadas/inseridas. A forma para identificar esta funcionalidade nos atributos sera com a marcação do coringa # (jogo da velha ao lado do atributo).

#### Abaixo um Exemplo no schema de pessoa.

#### **EX: Schemma Pessoa atribudo GHE.**

<br>


#### Este campo aceita a realização de merge das informações, ou seja, se informado o valor CHAVE {id: 0} no objeto o Integrador entende que este campo não deve apagar as informações já contidas nele. Cenario: Valores onde foram inseridos manualmente pelo Sistema Apollus e a informação não existe por parte do consumidor do WS.

#### Para Schemma complexos utilizar a estrutura:

    {
               id:0
    }
	
#### Para atributos simples como:

<br>
 
#### **String**

#### - Informando NULL o Integrador mantem o valor existente no Apollus.
#### - Informando “” (Duas aspas vazias) o Integrador apaga a informação existente no Apollus.

<br>

#### **Numérico** (Integer, Double, Long)

#### - Informando NULL o Integrador mantem o valor existente no Apollus.
#### - Informando -999999 o Integrador apaga a informação existente no Apollus.

## Lista Auxiliar EPI

#### Abaixo segue uma lista dos códigos “hardcode” utilizados no serviço de EPI. 

<br>

<table border="1">

   <tr>
   <td><b> Código </b></td> 
   <td><b> Descrição</b></td>  
   </tr>
   
   <tr>
   <td>  PA</td> 
   <td>  Proteção Auditiva.  </td>
   </tr>
  
   <tr>
   <td>  CO</td> 
   <td>  Concha</td>
   </tr>
   
   <tr>
   <td>  IM</td> 
   <td>  Inserção Moldável</td>
   </tr>
   
   <tr>
   <td>  IP</td> 
   <td>  Inserção Pré-Moldado</td>
   </tr>
   
   <tr>
   <td>  MI</td> 
   <td>  Proteção Membros Inferiores</td>
   </tr>
   
   <tr>
   <td>  CP</td> 
   <td>  Calça</td>
   </tr>
   
   <tr>
   <td>  PA</td> 
   <td>  Palmilha</td>
   </tr>
   
   <tr>
   <td>  PE</td> 
   <td>  Perneira</td>
   </tr>
   
   <tr>
   <td>  ME</td> 
   <td>  Meia</td>
   </tr>
   
   <tr>
   <td>  CD</td> 
   <td>  Calção</td>
   </tr>
   
   <tr>
   <td>  MS</td> 
   <td>  Proteção Membros Superiores</td>
   </tr>
   
   <tr>
   <td>  CP</td> 
   <td>  Creme Protetor</td>
   </tr>
   
   <tr>
   <td>  BR</td> 
   <td>  Braçadeira</td>
   </tr>
   
   <tr>
   <td>  DD</td> 
   <td>  Dedeira</td>
   </tr>
   
   <tr>
   <td>  MG</td> 
   <td>  Manga</td>
   </tr>
   
   <tr>
   <td>  LU</td> 
   <td>  Luvas</td>
   </tr>
   
   <tr>
   <td>  OF</td> 
   <td>  Proteção Olhos e Face</td>
   </tr>
   
   <tr>
   <td>  LM</td> 
   <td>  Lente Mascara</td>
   </tr>
   
   <tr>
   <td>  LO</td> 
   <td>  Lente Óculos</td>
   </tr>
   
   <tr>
   <td>  OC</td> 
   <td>  Óculos</td>
   </tr>
   
   <tr>
   <td>  PF</td> 
   <td>  Proteção Facial</td>
   </tr>
   
   <tr>
   <td>  MS</td> 
   <td>  Máscara Soldador</td>
   </tr>
   
   <tr>
   <td>  CA</td> 
   <td>  Proteção para Cabeça</td>
   </tr>
   
   <tr>
   <td>  CE</td> 
   <td>  Capacete</td>
   </tr>
   
   <tr>
   <td>  CZ</td> 
   <td>  Capuz</td>
   </tr>
   
   <tr>
   <td>  JU</td> 
   <td>  Jugular</td>
   </tr>
   
   <tr>
   <td>  TO</td> 
   <td>  Touca</td>
   </tr>
   
   <tr>
   <td>  TA</td> 
   <td>  Proteção para Trabalho em Altura</td>
   </tr>
   
   <tr>
   <td>  CI</td> 
   <td>  Cinturão</td>
   </tr>
   
   <tr>
   <td>  TA</td> 
   <td>  Talabarte</td>
   </tr>
   
   <tr>
   <td>  TR</td> 
   <td>  Proteção Tronco</td>
   </tr>
   
   <tr>
   <td>  CO</td> 
   <td>  Colete</td>
   </tr>
   
   <tr>
   <td>  VS</td> 
   <td>  Vestimenta</td>
   </tr>
   
   <tr>
   <td>  MA</td> 
   <td>  Macacão</td>
   </tr>
   
   <tr>
   <td>  AC</td> 
   <td>  Acessórios</td>
   </tr>
   
   <tr>
   <td>  CP</td> 
   <td>  Creme Protetivo</td>
   </tr>
   
   <tr>
   <td>  PO</td> 
   <td>  Pochete</td>
   </tr>
   
   <tr>
   <td>  OU</td> 
   <td>  Outros</td>
   </tr>
   
</table>

<br>

 <center> <h3> [Início](/manual-de-integração/apollus-integracao-api-rest-versao-1.0/glossário/) </h3> </center>

<center> <h3> <b> [Sumário] (/manual-de-integração/) </b> </center>
