# testing
test
<select name="bedrijf_id">
    <?php
    foreach($bedrijven as $bedrijf) {
        echo "<option value='" . $bedrijf['ID'] . "'>" . $bedrijf['naam'] . "</option>";
    }
    ?>
</select>
