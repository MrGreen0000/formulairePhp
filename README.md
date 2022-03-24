# formulairePhp

###Code form.php : Formulare

<form  action="reponse.php"  method="POST">

    <div>

      <label  for="nom">Nom :</label>

      <input  type="text"  id="nom"  name="last_name" placeholder="Nom" require>

    </div>
    <div>

      <label  for="prenom">Prénom :</label>

      <input  type="text"  id="prenom"  name="first_name" placeholder="Prénom" require>

    </div>
    <div>
    <label for="sujet">Choisie un sujet :</label>
        <select id="sujet" name="sujet">
          <option value="Histoire">L'histoire</option>
          <option value="Mathematique"> Les mathematiques</option>
        <option value="Philosophie">La philosophie</option>
        </select>
    </div>
    <div>

      <label  for="email">Email :</label>

        <input  type="email"  id="email"  name="email" placeholder="Email" require>

    </div>
    <div>

      <label  for="telephone">Téléphone :</label>

        <input  type="number"  id="telephone"  name="call_number" placeholder="Téléphone" require>

    </div>

    <div>

      <label  for="message">Message :</label>

      <textarea  id="message"  name="message" placeholder="Ecrit ton message" require></textarea>

    </div>

    <div  class="button">

      <button  type="submit">Envoyer</button>

    </div>

  </form>
  
  
###Code reponse.php : reponse
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
</head>

<body>
  
  
  <main>
    
      <?php 
        echo "<p> Merci " .$_POST["first_name"] . " " . $_POST["last_name"] .
        " de nous avoir contacté à propos de ce thème :". " " .$_POST["sujet"]."." . "</p>" ."<br>" ;
        echo "<p>Un de nos conseiller vous contactera soit à l’adresse " . $_POST["email"] . " " .
        "ou par téléphone au :" . " ". $_POST["call_number"] . " " .  "dans les plus brefs délais pour traiter votre demande :" .
        " " . $_POST["message"]."." . "</p>"; 
        ?>
    </div>
  </main>

</body>
</html>

