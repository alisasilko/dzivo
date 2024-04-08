class ProjektuMerki:
    def __init__(self):
        self.merki = [
            "Stimulēt sabiedrības izpratni par veselīgu un līdzsvarotu dzīvesveidu.",
            "Sniedzēt vispusīgu informāciju par veselīgu uzturu, fizisko aktivitāti, emocionālo labklājību un citiem faktoriem, kas veicina labu dzīvesveidu.",
            "Piedāvāt motivējošus stāstus, piemērus un praktiskus padomus, lai cilvēki justos iedvesmoti un gatavi veikt pozitīvas izmaiņas savā dzīvē.",
            "Nodrošināt receptes, treniņu plānus, meditācijas vadības un tām līdzīgus praktiskus rīkus, kas palīdzēs cilvēkiem integrēt veselīgus paradumus savā ikdienas rutīnā.",]

    def izvadit_merkus(self):
        print("Projekta mērķi:")
        for i, merkis in enumerate(self.merki, start=1):
            print(f"{i}. {merkis}")

class MobilāLietotne:
    def __init__(self):
        self.uzdevumi = []

    def pievienot_uzdevumu(self, nosaukums, apraksts):
        self.uzdevumi.append({"nosaukums": nosaukums, "apraksts": apraksts})

    def izvadit_uzdevumus(self):
        print("Uzdevumi:")
        for i, uzdevums in enumerate(self.uzdevumi, start=1):
            print(f"{i}. {uzdevums['nosaukums']}: {uzdevums['apraksts']}")


class TreniņuPlāns:
    def __init__(self):
        self.plani = []

    def pievienot_planu(self, nosaukums, apraksts):
        self.plani.append({"nosaukums": nosaukums, "apraksts": apraksts})

    def izvadit_planus(self):
        print("\nTreniņu plāni:")
        for i, plans in enumerate(self.plani, start=1):
            print(f"{i}. {plans['nosaukums']}: {plans['apraksts']}")


# Izveidojam mobilās lietotnes objektu un pievienojam uzdevumus
lietotne = MobilāLietotne()
lietotne.pievienot_uzdevumu("Skaitīt kalorijas", "Skaitīt kaloriju patēriņu dienu laikā")
lietotne.pievienot_uzdevumu("Izveidot treniņu plānu", "Izveidot pilnīgu un funkcionējošu treniņu plānu ar treniņu piemēriem un treneru padomiem")

# Izvadīt uzdevumus
lietotne.izvadit_uzdevumus()

# Izveidojam treniņu plānu objektu un pievienojam treniņu plānus
plani = TreniņuPlāns()
plani.pievienot_planu("Kardio treniņu plāns", "Plāns, kas iekļauj kardio vingrinājumus, piemēram, skriešanu vai veloergometra izmantošanu")
plani.pievienot_planu("Spēka treniņu plāns", "Plāns, kas iekļauj spēka vingrinājumus, piemēram, svaru celšanu vai elastību vingrinājumus")

# Izvadīt treniņu plānus
plani.izvadit_planus()


class AnketuJautajumi:
    def __init__(self):
        self.jautajumi = [
            "Vai jūs skaitāt kalorijas?",
            "Cik daudz ūdens glāzes jūs dzerat dienā?",
            "Vai jūs gribat samazināt sava ķērmeņa svaru?",
            "Cik daudz soļus jūs staigājat dienā?"
        ]

    def izvadit_jautajumus(self):
        print("\nAnketu jautājumi:")
        for i, jautajums in enumerate(self.jautajumi, start=1):
            print(f"{i}. {jautajums}")


class AptaujasRezultati:
    def __init__(self, rezultati):
        self.rezultati = rezultati

    def izvadit_rezultatus(self):
        print("\nAptaujas rezultāti:")
        for rezultats in self.rezultati:
            print(rezultats)


# Izveidojam objektus un izvadām informāciju
projekta_merki = ProjektuMerki()
projekta_merki.izvadit_merkus()

anketu_jautajumi = AnketuJautajumi()
anketu_jautajumi.izvadit_jautajumus()

# Pieņemsim, ka aptaujas rezultāti ir saraksts ar teksta rezultātiem
apt_rezultati = [
    "Aptaujas rezultāti rāda, ka 33,3% respondentu regulāri skaita kalorijas katru dienu, bet 19% to dara dažreiz.",
    "Pēc otrā aptaujas jautājuma varam spriest, ka ne visiem ir līdzīgs ūdens patēriņš dienā.",
    "Uz jautājumu, vai cilvēki vēlas samazināt savu svaru, vairāk nekā puse aptaujāto atbildēja, ka vēlas.",
    "Uz jautājumu, cik soļus veic respondenti, 38% (vairākums) atbildēja, ka vidēji veic 5000 soļu."
]

apt_rezultati_obj = AptaujasRezultati(apt_rezultati)
apt_rezultati_obj.izvadit_rezultatus()

