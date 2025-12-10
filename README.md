from IPython.display import HTML, display

html_code = """
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Generador médico</title>
  <style>
    input, textarea {width:100%; padding:8px; margin:6px 0;}
  </style>
</head>
<body>
  <h2>Generador de texto clínico</h2>

  <input id="medico" placeholder="Nombre del médico">
  <input id="tarjeta" placeholder="Tarjeta profesional">
  <input id="paciente" placeholder="Nombre del paciente">
  <input id="cedula" placeholder="Cédula del paciente">
  <input id="municipio" placeholder="Municipio y departamento">
  <input id="discapacidad" placeholder="Tipo de discapacidad">
  <input id="diagnostico" placeholder="Diagnóstico">
  <input id="cie10" placeholder="Código CIE-10">

  <button onclick="generar()">Generar</button>

  <textarea id="resultado"></textarea>

  <script>
    function generar(){
      let medico = document.getElementById("medico").value;
      let tarjeta = document.getElementById("tarjeta").value;
      let paciente = document.getElementById("paciente").value;
      let cedula = document.getElementById("cedula").value;
      let municipio = document.getElementById("municipio").value;
      let discapacidad = document.getElementById("discapacidad").value;
      let diagnostico = document.getElementById("diagnostico").value;
      let cie10 = document.getElementById("cie10").value;

      let texto = `Yo, ${medico}, Médico General con Tarjeta Profesional N° ${tarjeta}, certifico que el paciente ${paciente}, identificado con C.C. ${cedula}, domiciliado en ${municipio}, presenta ${discapacidad} con diagnóstico ${diagnostico} (CIE-10: ${cie10}).`;

      document.getElementById("resultado").value = texto;
    }
  </script>
</body>
</html>
"""

display(HTML(html_code))
