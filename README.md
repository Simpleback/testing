# testing
test
1 flier
<select name="bedrijf_id">
    <?php
    foreach($bedrijven as $bedrijf) {
        echo "<option value='" . $bedrijf['ID'] . "'>" . $bedrijf['naam'] . "</option>";
    }
    ?>
</select>

2 werkver
// de value die je ophaalt uit de select box
$bedrijf_ID = $_POST['bedrijf_ID']; 

// die voeg je toe bij de query
$result = mysqli_query($mysql, "INSERT INTO studenten (alle velden, bedrijf_id) VALUES ('$blabla', '$bedrijf_ID')");

3ophel

function bedrijf() 
{
    // $_GET['id'] is de id die hij meeneemt uit de url op detail pagina
    $bedrijf_id = mysqli_query($mysql, "SELECT * FROM studenten WHERE id = '" . $_GET['id'] . "'");
    $studenten = mysqli_fetch_array($bedrijf_id);

    $bedrijf = mysqli_query($mysql, "SELECT * FROM bedrijven WHERE id = '" . $studenten['bedrijf_ID'] . "'");
    return mysqli_fetch_array($bedrijf);

}



4 ervmak
$ervaring = $_POST['ervaring'];

$id = $_SESSION['student_session']; // of hoe je het ook hebt genoemd. Gewoon de huidige sessie van de ingelogde persoon ophalen

$bedrijf = mysqli_query($mysql, "SELECT bedrijf_id FROM studenten WHERe id = '" . $id . "'");

$result = mysqli_fetch_array($bedrijf);
$bedrijf_ID = $result['bedrijf_ID'];

$result = mysqli_query($mysql, "INSERT INTO ervaringen(ervaring, student_id, bedrijf_id) VALUES('$ervaring', '$id', '$bedrijf_ID')");
