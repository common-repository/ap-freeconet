
Aby uruchomi� kontrolk� FlashCall na swojej stronie:
----------------------------------------------------
1. Pobra�e� i rozpakowa�e� ju� plik flashcall.zip, wi�c wszystkie pliki umie�� na serwerze, w katalogu z Twoj� stron� www. Pliki musz� si� znale�� w g��wnym katalogu Twojej strony (tam, gdzie znajduje si� plik index.php lub index.html). Je�eli nie potrafisz tego zrobi�, zwr�� si� do osoby, kt�ra stworzy�a dla Ciebie stron� www. Je�eli chcesz umie�ci� pliki FlashCall'a w jakim� podkatalogu, zobacz temat "Modyfikacja wygenerowanego kodu".
2. Skopiuj kod, kt�ry wygenerowa�e� w swoim panelu FreecoNet na ekranie "Konfiguracja -> Dodatki -> FlashCall". Je�eli  zapomnia�e� skopiowa� kodu, mo�esz go teraz ponownie wygenerowa� na wspomnianym ekranie.
3. Wklej kod na swoj� stron� w miejscu, w kt�rym chcesz umie�ci� kontrolk� FlashCall.



Chc� umie�ci� na swojej stronie wi�cej ni� jedn� kontrolk� FlashCall:
---------------------------------------------------------------------
W takim przypadku po prostu wygeneruj kod dla kolejnej kontrolki i umie�� na swojej stronie. Pami�taj, �e ka�da kontrolka powinna zestawia� po��czenie z innym kontem FreecoNet.



Co� nie dzia�a? Upewnij si�:
----------------------------
- Czy podczas konfiguracji kontrolki wybra�e� prawid�owe konto w polu "Po��cz z kontem"? Upewnij si�, czy na wybrane przez Ciebie konto mo�na si� dodzwoni�.
- Czy na pewno skopiowa�e� ca�y kod jaki dla Ciebie wygenerowali�my? Je�li nie jeste� pewien, wygeneruj go ponownie, kliknij prawym klawiszem myszki w okienko z kodem i wybierz "Zaznacz wszystko". Skopiuj kod (Ctrl+C) oraz wklej (Ctrl+V) ponownie na swoj� stron�.
- Czy umie�ci�e� wszystkie rozpakowane pliki w g��wnym katalogu Twojej strony? Te pliki to: flashcall.swf, FlashCallF.lib, FlashCallS.lib. Nie umieszczaj ich w �adnym podkatalogu np. "flash". Powinny znale�� si� w tym samym katalogu, w kt�rym znajduje si� plik index.php (lub index.html). Je�eli chcesz umie�ci� pliki FlashCall'a w jakim� podkatalogu, zobacz temat "Modyfikacja wygenerowanego kodu".

Je�eli zrobi�e� wszystko poprawnie a mimo to kontrolka FlashCall nie dzia�a, w�wczas napisz do nas na service@freeconet.pl podaj�c adres strony www, na kt�r� pr�bowa�e� wstawi� kontrolk� FlashCall.




Modyfikacja wygenerowanego kodu:
--------------------------------
Je�eli jeste� zaawansowanym u�ytkownikiem, mo�esz sam modyfikowa� wygenerowany kod za pomoc� parametr�w:
<param name="flashvars" value="parametr1=warto��&parametr2=warto��...">

Mo�esz ustawi� nast�puj�ce parametry:

id=IDENTYFIKATOR
Ustawia identyfikator kontrolki FlashCall. Musi on odpowiada� parametrom id oraz name znacznika <object>. W przypadku umieszczenia na stronie wi�cej ni� jednej kontrolki FlashCall, ich identyfikatory musz� si� r�ni�. Domy�lnie generowanym identyfikatorem jest "flascall_NAZWAKONTA".

auth_domain=DOMENA
Ustawia domen� sip. Domy�lnie generowan� domen� jest "sip.vectrabiznes.pl" i nie powinna by� ona zmieniana.

user=NAZWA_KONTA
Ustawia konto NAZWA_KONTA, z kt�rym zostanie zestawione po��czenie.

keyboard=on/off
Ustawia, czy ma by� widoczna klawiatura numeryczna po nawi�zaniu po��czenia. Ustaw "on" aby w��czy� klawiatur� lub "off" aby j� wy��czy�.

label=TEKST_TYTU�OWY
Ustawia tekst tytu�owy widoczny obok zielonego przycisku ze s�uchawk�.

info_text=TEKST_DODATKOWY
Ustawia dodatkowy tekst widoczny pod zielonym przyciskiem ze s�uchawk�.

text=TEKST_OPISU
Ustawia dodatkowy tekst opisu, widoczny po klikni�ciu na "wi�cej".

lang=pl/en
Ustawia j�zyk komunikat�w wy�wietlanych przez FlashCall. Mo�liwe opcje to: pl - j�zyk polski (domy�lnie), en - j�zyk angielski.

Istnieje r�wnie� funkcja javascript, za pomoc� kt�rej mo�esz zmieni� �cie�k� z zasobami FlashCall'a (pliki FlashCallF.lib oraz FlashCallS.lib):

function getLibPath() { return "�CIE�KA"; }

�cie�k� mo�na poda� w postaci nazwy podkatalogu lub adresu URL. Je�eli chcia�by� umie�ci� pliki FlashCall'a np. w podkatalogu "/swf/flashcall" w�wczas wywo�aj nast�puj�c� funkcj�:

<script type="text/javascript">
function getLibPath() { return "swf/flashcall"; }
</script>
