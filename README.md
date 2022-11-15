<!DOCTYPE html>
<html lang="en">

<head>
       <meta charset="UTF-8">
       <meta http-equiv="X-UA-Compatible" content="IE=edge">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Document</title>
       <script src="jwifi.js"></script>
       <script>
              function check() {
                     var valor = document.getElementById("txtValor").value;
                     var datanct = /^\d{2}\/\d{2}\/\d{4}$/;
                     if (datanct.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function validar() {
                     var valor = document.getElementById("txtCodigo").value;
                     var cpf = /^\d{3}\.\d{3}\.\d{3}\-\d{2}$/;
                     if (cpf.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function verificar() {
                     var valor = document.getElementById("txtCodigos").value;
                     var nummt = /^IFTM-\d{3}\/\d{3}\-\w{2}$/;
                     if (nummt.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function valores() {
                     var valor = document.getElementById("txtCodMatric").value;
                     var codmat = /^MT-\d{2}\.\d{3}\-IFTM$/i;
                     if (codmat.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function valoresT() {
                     var valor = document.getElementById("txtCodMatricT").value;
                     var codmatT = /^MT-\d{2}\.\d{3}\-(I|i)(F|f)(T|t)(M|m)$/;
                     if (codmatT.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function valoresS() {
                     var valor = document.getElementById("txtCodMatricS").value;
                     var codmatS = /^M\s?T\s?-\d{2}\-\d{3}\-I\s?F\s?T\s?M$/i;
                     if (codmatS.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function valoresG() {
                     var valor = document.getElementById("txtCodMatricG").value;
                     var codmatG = /^(M|m)\s?(T|t)\s?\-\d{2}\.\d{3}\-(I|i)\s?(F|f)\s?(T|t)\s?(M|m)\s?(Uberlândia|Uberlândia Centro)$/;
                     if (codmatG.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function valoresH() {
                     var valor = document.getElementById("txtCodMatricH").value;
                     var codmatH = /^(IFTM campus Uberlândia|IFTM campus Uberlândia Centro)$/;
                     if (codmatH.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function validarI() {
                     var valor = document.getElementById("txtCodigoI").value;
                     var telef = /^\+\d{2}\(\d{2}\)\d{5}-\d{4}$/;
                     if (telef.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function validarJ() {
                     var valor = document.getElementById("txtCodigoJ").value;
                     var telefJ = /^\(\d{2}\)\d{5}-\d{4}$/;
                     if (telefJ.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function validarK() {
                     var valor = document.getElementById("txtCodigoK").value;
                     var altura = /^[1](.|,)[3-9]|[1](.|,)[3-9][0-9]|[2](.|,)[5][0]|[2](.|,)[0-4][0-9]|[2](.|,)[5]$/;
                     if (altura.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function validarL() {
                     var valor = document.getElementById("txtCodigoL").value;
                     var receita = /^(R\$)[0-9]{1}[0-9]{0,2}(\.[0-9]{3}){0,3}(\,[0-9]{1,2})$/;
                     if (receita.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function validarM() {
                     var valor = document.getElementById("txtCodigoM").value;
                     var codometro = /^([01]?[0-9]|2[0-3]):[0-5][0-9](:[0-5][0-9]):[0-9][0-9]?$/;
                     if (codometro.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
              function validarN() {
                     var valor = document.getElementById("txtCodigoN").value;
                     var senha = /^[A-Za-z0-9.-_]{5,}&[A-Pa-p]{1,}\.[a-z]{1,}\.[A-Za-z0-5]{1,}-[^0-9]{1,},[^A-Za-zÀ-ú0-9]{2}.[^ab01]{1,}$/;
                     if (senha.test(valor)) {
                            alert("Padrão válido");
                     }
                     else {
                            alert("Padrão inválido")
                     }
              }
       </script>
</head>

<body>
       <form>
              <form>
                     <label>Data Nacimento:</label>
                     <input type="text" id="txtValor" value="30/12/1999">
                     <input type="button" value="Verificar" onclick="check()">
              </form>
              <br><br><br><br>
              <form>
                     <label>CPF:</label>
                     <input type="text" id="txtCodigo" value="123.456.789-00"
                            onkeypress="inserirMascara('txtCodigo','999.999.999-99')">
                     <input type="button" value="Verificar" onclick="validar()">
              </form>

              <br><br><br><br>
              <form>
                     <label>Número de matrícula de um aluno:</label>
                     <input type="text" id="txtCodigos" value="IFTM-000/000-00">
                     <input type="button" value="Verificar" onclick="verificar()">
              </form>
              <br><br><br><br>

              <form>
                     <label>Código de uma disciplina do IFTM (jwifi):</label>
                     <input type="text" id="txtCodMatric" value="MT-99.999-IFTM"
                            onkeypress="inserirMascara('txtCodMatric','MT-99.999-IFTM')">
                     <input type="button" value="Verificar" onclick="valores()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Código de uma disciplina do IFTM versão2 (jwifi):</label>
                     <input type="text" id="txtCodMatricT" value="MT-99.999-IFTM"
                            onkeypress="inserirMascara('txtCodMatricT','MT-99-999-IFTM')">
                     <input type="button" value="Verificar" onclick="valoresT()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Código de uma disciplina do IFTM (versão 3):</label>
                     <input type="text" id="txtCodMatricS" value="MT-99-999-IFTM">
                     <input type="button" value="Verificar" onclick="valoresS()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Código de uma disciplina do IFTM (versão 4):</label>
                     <input type="text" id="txtCodMatricG" value="MT-99.999-IFTM Uberlândia">
                     <input type="button" value="Verificar" onclick="valoresG()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Nome de campus do IFTM:</label>
                     <input type="text" id="txtCodMatricH" value="IFTM campus Uberlândia">
                     <input type="button" value="Verificar" onclick="valoresH()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Telefone:</label>
                     <input type="text" id="txtCodigoI" value="+55(34)99880-2552"
                            onkeypress="inserirMascara('txtCodigoI','+99(99)99999-999')">
                     <input type="button" value="Verificar" onclick="validarI()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Telefone (versão 2):</label>
                     <input type="text" id="txtCodigoJ" value="(34)99880-2552">
                     <input type="button" value="Verificar" onclick="validarJ()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Altura de uma pessoa:</label>
                     <input type="text" id="txtCodigoK" value="1,69">
                     <input type="button" value="Verificar" onclick="validarK()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Faturamento anual de uma empresa:</label>
                     <input type="text" id="txtCodigoL" value="R$999.999.999.999,99">
                     <input type="button" value="Verificar" onclick="validarL()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Cronômetro (jwifi):</label>
                     <input type="text" id="txtCodigoM" value="22:22:22:22">
                     <input type="button" value="Verificar" onclick="validarM()">
              </form>
              <form>
                     <br><br><br><br>
                     <label>Senha:</label>
                     <input type="password" id="txtCodigoN" value="321a.&apMb.aei.Ab0-asf+_,/*.cq">
                     <input type="button" value="Verificar" onclick="validarN()">
              </form>
       </form>
</body>

</html>
