1. 17-aastane ei saa autot rentida
-- sisendite kombinatsioon: vanus: 17, [...]
-- oodatav väljund: Exception("Driver too young - cannot quote the price")

2. 18-aastane saab autot rentida
-- sisendite kombinatsioon: vanus: 18, [...]
-- oodatav väljund: hind 18-aastasele XXX EUR

3. 18-21 aastane saab autot rentida, mis kuulub klassi 1
-- sisendite kobinatsioon: vanus: 18 või 19 või 20 või 21; auto klass: 1;
--oodatav väljund: hind 18 või 19 või 20 või 21 aastasele 1. klassi autole on XXX EUR.

4. 18-21 aastane ei saa autot rentida, mis kuulub klassi 2-5
--sisendite kombinatsioon: vanus: 18 või 19 või 20 või 21; auto klass: 2 või 3 või 4 või 5;
--oodatav väljund: Exception("Drivers 21 y/o or less can only rent Class 1 vehicles")

5. Maksimaalne rendi hind on 1000€
--sisendite kombinatsioon: rendi_hind = 1300€
--oodatav väljund: auto rendi hinnaga 1000€

6. Juhil peab olema vähemalt 1-aastased load.
--sisendite kombinatsioon: Juhiload aastates: 0,5
--oodatav väljund: Exception("Driver must hold driving licence at least for one year. Can not rent a car!")

7. Juhil on alla kolme aastased load:
--sisendite arv: juhiload aastates: 2,5
--oodtav väljund rendi hind on 1.3 * XXX EUR

8. Juhil on üle kolme aasta load olnud, pole õnnetusi teinud ning on 32-aastane:
--sisendite arv: juhiload aastates: 3.8, vanus: 32, acc = false.
--oodatav väljund: rendihind on XXX EUR.

9. Juhil on üle kolme aasta load olnud, pole õnnetuses osalenud ning on 24-aastane ja rendib 4 klassi autot:
--sisendite arv: juhiload aastates: 3.8, vanus: 24, acc = false, clazz = 4.
--oodatav väljund: rendihind on 2 * XXX EUR.

10. Juhil on üle kolme aasta load olnud, on õnnetuses osalenud ning on 24-aastane ja rendib 4 klassi autot:
--sisendite arv: juhiload aastates: 3.8, vanus: 24, acc = true, clazz = 4.
--oodatav väljund: rendihind on 2 *(15 + XXX EUR)

11. Juht on 47-aastane aga auto päevarendi hind on 33€.
--sisendite arv: päevarendihind: 33, vanus: 47,
--oodatav väljund: päevarendihind = vanus, päevarendihind = 47:

12. Juht on 29-aastane aga auto päevarendi hind on 33€.
--sisendite arv: päevarendihind: 33, vanus: 29,
--oodatav väljund: päevarendihind = 33:
