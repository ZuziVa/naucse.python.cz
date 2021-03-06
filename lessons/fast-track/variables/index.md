# Proměnné

Důležitým konceptem v programování jsou *proměnné*.
Proměnná není nic jiného než *pojmenování* něčeho,
co budeme chtít použít později.
Programátoři proměnné používají k ukládání dat,
aby byl jejich kód čitelnější a nemuseli si pamatovat konkrétní hodnoty.

Řekněme, že chceš řetězec se svým jménem pojmenovat jako `jmeno`.
To se zapíše takto:

``` pycon
>>> jmeno = 'Ola'
```

Proměnná `jmeno` teď bude mít hodnotu `'Ola'`.

Jak sis mohl{{a}} všimnout, tenhle příkaz nic nevrátil – Python nevypsal
žádný výsledek.
Jak pak zjistíš, že proměnná skutečně existuje?

Zadej samotné jméno proměnné (tedy `jmeno`, bez uvozovek) a stiskni
<kbd>Enter</kbd>:

``` pycon
>>> jmeno
'Ola'
```

Zkus si nastavit i jinou proměnnou – třeba svoji oblíbenou barvu:

``` pycon
>>> barva = 'modrá'
>>> barva
'modrá'
```

Kdykoli můžeš do proměnné přiřadit znovu a změnit tak co se pod
daným jménem skrývá:

``` pycon
>>> jmeno
'Ola'
>>> jmeno = "Soňa"
>>> jmeno
'Soňa'
```

Můžeš ji také předat funkci nebo použít ve výrazu.
Python za jméno proměnné dosadí aktuální hodnotu:

``` pycon
>>> len(jmeno)
4
>>> jmeno * 4
'SoňaSoňaSoňaSoňa'
```

Super, ne?

Proměnná může obsahovat cokoliv, například i čísla.
Zkus tohle:

``` pycon
>>> sirka = 4
>>> delka = 6
>>> sirka * delka
24
```

Ale co když použiješ nesprávné jméno? Dokážeš odhadnout, co se stane?

{% filter solution %}
``` pycon
>>> mesto = "Tokyo"
>>> mmesto
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'mmesto' is not defined
```
{% endfilter %}

Chyba!

Python má různé typy chyb. Tato se nazývá `NameError`.
Python ti vrátí tuto chybu, pokud se pokusíš použít proměnnou,
která dosud nebyla nastavena.
Často jde o překlep.
Když tedy uvidíš `NameError` zkontroluj jestli jsi neudělal{{a}} překlep,
když jsi proměnnou nastavovala nebo použila.


## Jména proměnných
Profesionální programátoři pojmenovávají proměnné anglicky,
aby jim rozumělo co nejvíc kolegů po celém světě.
Začátečníkům ale doporučujeme češtinu – je tak jasnější, která jména
si můžeš zvolit {{gnd('sám', 'sama')}} (např. `barva`) a která jsou
z Pythonu (např. `upper`).
Nevýhoda je, že si časem budeš muset odvyknout.


Každopádně je dobré nepoužívat diakritiku a vyhnout se velkým pímenům:
místo <code><strong>J</strong>m<strong>é</strong>no</code> použij jen `jmeno`.


Vyzkoušej si:
Která z těchto jmen ti Python dovolí použít jako proměnnou?

* `tlacitko5`
* `5tlacitko`
* `tlačítko`
* `oblibena barva`
* `oblibena-barva`
* `oblibenaBarva`

{% filter solution %}

* `tlacitko5` ano.
* `5tlacitko` ne: jména musí začínat písmenkem.
* `tlačítko` ano, ale diakritice (`č`, `í`) je lepší se vyhnout.
* `oblibena barva` ne: to není jedno jméno, ale dvě!
* `oblibena-barva` taky ne: to Python bere jako odečtení dvou proměnných
  (`oblibena` mínus `barva`).
* `oblibenaBarva` ano, ale velkým písmenům je lepší se vyhnout.
{% endfilter %}

Ve složitějších jménech proměnných se používá podtržítko.
Např. `oblibena_barva` bude Python považovat za jedno slovo, název jedné
proměnné, ale člověk vidí slova dvě.

``` pycon
>>> oblibena_barva = 'žlutá'
>>> oblibena_barva.upper()
'ŽLUTÁ'
```


## Shrnutí

* **Proměnné** jsou jména pro hodnoty.
* Přiřazením (`=`) můžeš proměnnou nastavit na jakoukoli hodnotu.
* Proměnné pojmenováváme **malými písmenky** bez diakritiky.
* Na oddělení slov v rámci jména můžeme použít **podtržítko**.
