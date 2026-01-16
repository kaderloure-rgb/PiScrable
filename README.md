# PiScrable
PiScrable combine Scrabble et un vocabulaire spécialisé en crypto monnaie . Jouez, apprenez, marquez des points et gagnez du Pi en formant des mots intelligents sur la blockchain. Defiez vos amis !
<!DOCTYPE html>
<html>
<head>
  <title>PScrable</title>
  <script src="https://sdk.minepi.com/pi-sdk.js"></script>
</head>
<body>
  <h1>PScrable</h1>
  <button onclick="login()">Se connecter avec Pi</button>

  <script>
    Pi.init({ version: "2.0" });

    function login() {
      Pi.authenticate(
        ["username"],
        function(auth) {
          alert("Bienvenue " + auth.user.username);
        },
        function(error) {
          alert("Erreur Pi");
        }
      );
    }
  </script>
</body>
</html>
