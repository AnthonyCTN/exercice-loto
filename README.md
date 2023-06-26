# exercice-loto
random number generator for lotto made in javascript


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

    <h1>Générateur de nombres aléatoires</h1>
  <button onclick="genererNombres()">Générer</button>
  <p id="resultat"></p>

  <script >
    function genererNombres() {
  let nombres = [];

  while (nombres.length < 6) {
    const nombreAleatoire = Math.floor(Math.random() * 49) + 1;

    if (!nombres.includes(nombreAleatoire)) {
      nombres.push(nombreAleatoire);
    }
  }

  const resultat = document.getElementById('resultat');
  resultat.textContent = nombres.join('-');
}

  </script>
    
</body>
</html>

<style>
    body {
  font-family: Arial, sans-serif;
  text-align: center;
}

h1 {
  color: #333;
}

button {
  padding: 10px 20px;
  font-size: 16px;
}

#resultat {
  font-size: 20px;
  margin-top: 20px;
}

</style>
