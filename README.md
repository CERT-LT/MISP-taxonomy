# MISP taksonomija

`lt-cyber-incidents-tax-pub.json` - Kibernetinių incidentų taksonomija parengta pagal nacionalinį kibernetinių incidentų valdymo planą - https://www.e-tar.lt/portal/lt/legalAct/c8e268a0a00011efa605b9842742bf37  (18 punktas)

## Kaip įsidiegti NKSC taksonomiją savo MISP serveryje

### Serveryje

1. Pereikite į MISP taksonomijų katalogą:
   ```bash
   cd /var/www/MISP/app/files/taxonomies/
   ```

2. Sukurkite naują katalogą pavadinimu "nksc":
   ```bash
   mkdir nksc
   ```

3. Pakeiskite naujai sukurto katalogo savininką į www-data:
   ```bash
   chown -R www-data:www-data nksc
   ```

4. Atidarykite "machinetag.json" failą redagavimui:
   ```bash
   vim machinetag.json
   ```

5. Nukopijuokite ir įklijuokite "machinetag.json" turinį iš CERT-LT GitHub repozitorijos (https://github.com/CERT-LT/MISP-taxonomy).

### MISP aplikacijoje

1. Eikite į "Event Actions" ir pasirinkite "List Taxonomies".

2. Spauskite "Update Taxonomies" mygtuką.

3. Atnaujintoje taksonomijų sąraše suraskite naujai įdiegtą NKSC taksonomiją.

4. Pasirinkite "Action enable all" naujai įdiegtai taksonomijai.

5. Galiausiai, sukurkite tagus pasirinkdami "enable all" iš "Active Tags" sekcijos.

Atlikus šiuos žingsnius, NKSC taksonomija bus sėkmingai įdiegta ir aktyvuota jūsų MISP serveryje.
