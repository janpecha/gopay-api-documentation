# Vyvolání nové platební brány
Pro vyvolání platební brány je možné použít HTML formulář, který pomocí javascriptu
provede inicializaci platební brány. 

## Inline varianta

>Formulář pro vyvolání inline platební brány

```html
<form action="https://gw.sandbox.gopay.com/gw/v3/dfgvmwTKK5hrJx2aGG8ZnFyBJhAvF"
  method="post" id="gopay-payment-button">
  <button name="pay" type="submit">Zaplatit</button>
  <script type="text/javascript" src="https://gw.sandbox.gopay.com/gp-gw/js/embed.js"></script>
</form>
```
Inline platební brána je vyvolána přímo nad portálem obchodníka, nedochází tedy k přesměrování.

URL (action) formuláře nastavte dle ```gw_url``` z [vytvoření platby](#založení-platby).

Parametr formuláře|Popis|Povinný
------------------|-----|--------
action|gw_url založené platby|ANO
method|HTTP metoda|ANO
id|id formuláře|ANO| Vždy nastaveno na gopay-payment-button

<aside class='notice'>
  Podrobný popis všech kroků nutných k vyvolání platební brány naleznete v našem <a href="https://help.gopay.com/cs/s/i4">centru nápovědy</a>
</aside>

## Redirect varianta

>Formulář pro přesměrování na Redirect platební bránu

```html
<form action="https://gw.sandbox.gopay.com/gw/v3/dfgvmwTKK5hrJx2aGG8ZnFyBJhAvF"
  method="post">
  <button name="pay" type="submit">Zaplatit</button>
</form>
```

Platební bránu lze provozovat i ve variantě s přesměrováním. Lze použít formulář viz níže
nebo provést přesměrování na URL předané při [vytvoření platby](#založení-platby) ```gw_url```.

Parametr formuláře|Popis|Povinný
-----------------|-----|--------
action|gw_url založené platby|ANO
method|HTTP metoda|ANO