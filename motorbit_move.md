Dobrý den, jistě. Na základě dostupných informací, které popisují programování micro:bitu v prostředí MakeCode (pomocí bloků) a práci s rozšiřujícími moduly, jako je Motor:bit, je možné navrhnout jednoduchý program, který splní váš požadavek.

Pro ovládání motorů pomocí desky **Motor:bit** je nutné do vývojového prostředí MakeCode importovat příslušný rozšiřující modul (`Motorbit`). Motor:bit je určen k řízení motorů robotických podvozků.

Zde je příklad programové logiky pro spuštění motoru a jeho zastavení po jedné sekundě. Tato sekvence by se měla ideálně umístit do bloku **`on start`** (při startu), aby se provedla pouze jednou. Protože však zdroje ukazují často kód v bloku `basic.forever` pro sekvenční akce s časovou prodlevou, ukážu sekvenci s použitím časových příkazů.

### Programová logika (MakeCode bloky)

Pro spuštění motoru na modulu Motor:bit můžete použít funkci **`motorbit.forward(rychlost)`**, kde rychlost je v rozsahu 0 až 100 (procenta výkonu). Pro časovou prodlevu se používá funkce **`basic.pause(ms)`**, kde $1$ sekunda odpovídá $1000$ milisekundám. Pro zastavení motoru se používá funkce **`motorbit.brake()`**.

Pokud byste programovali jednosměrný pohyb vpřed u robotického podvozku, mohla by se sekvence příkazů v MakeCode, vložená do bloku `on start`, skládat z následujících kroků (za předpokladu, že máte motor:bit rozšíření naimportované):

1.  **Start motoru:** Nastavte motor vpřed na určitou rychlost (např. 50 %).
    *Blok:* `motorbit.forward(50)`
2.  **Čekání:** Počkejte 1000 ms (1 sekundu).
    *Blok:* `basic.pause(1000)`
3.  **Stop motoru:** Zastavte motor.
    *Blok:* `motorbit.brake()`

### JavaScript Ekvivalent

Tato sekvence by se v jazyce **JavaScript** (který se zobrazí po přepnutí v MakeCode) mohla implementovat následovně (kód je upraven pro použití ve funkci, která se spustí při startu, nebo se jednorázově nachází v nekonečné smyčce `basic.forever`):

```javascript
basic.forever(function () {
    // START motoru
    motorbit.forward(50) 
    
    // Čekání 1 sekundu (1000 ms)
    basic.pause(1000) 
    
    // Zastavení motoru
    motorbit.brake() 
    
    // Protože je kód v nekonečné smyčce, přidáme dlouhou pauzu, 
    // aby se motor nespustil hned znovu.
    basic.pause(1000000) // Dlouhá pauza
})
```

**Vysvětlení kroků:**

💡 **motorbit.forward(50):** Spustí motory podvozku vpřed na 50 % výkonu.
💡 **basic.pause(1000):** Pozastaví provádění programu na $1000$ milisekund, tedy 1 sekundu.
💡 **motorbit.brake():** Okamžitě zastaví motory.

**Důležitá poznámka k hardware:**
Při práci s motory a servomotory je třeba si uvědomit, že mají relativně velký proudový odběr. Proto je obvykle nutné připojit externí zdroj napájení k rozšiřující desce (jako je Boson Expansion Board nebo Motor:bit), nikoliv spoléhat se pouze na napájení přes USB kabel micro:bitu.