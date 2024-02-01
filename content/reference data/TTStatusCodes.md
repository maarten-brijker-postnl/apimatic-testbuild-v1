# T & T Status Codes

# Status codes
    
<table>
  <thead>
    <tr>
      <th>Status code</th>
      <th>Phase</th>
      <th>Description NL</th>
      <th>Description EN</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1, Collectie</td>
      <td>Zending voorgemeld</td>
      <td>Shipment pre-alerted</td>
    </tr>
    <tr>
      <td>2</td>
      <td>1, Collectie</td>
      <td>Zending in ontvangst genomen</td>
      <td>Shipment accepted</td>
    </tr>
    <tr>
      <td>3</td>
      <td>1, Collectie</td>
      <td>Zending afgehaald</td>
      <td>Shipment collected</td>
    </tr>
    <tr>
      <td>4</td>
      <td>1, Collectie</td>
      <td>Zending niet afgehaald</td>
      <td>Shipment not collected</td>
    </tr>
    <tr>
      <td>13</td>
      <td>1, Collectie</td>
      <td>Voorgemeld: nog niet aangenomen</td>
      <td>Pre-alerted shipment</td>
    </tr>
    <tr>
      <td>14</td>
      <td>1, Collectie</td>
      <td>Voorgemeld: definitief niet aangenomen</td>
      <td>Shipment pre-alerted</td>
    </tr>
    <tr>
      <td>15</td>
      <td>1, Collectie</td>
      <td>Manco collectie</td>
      <td>Missing collection</td>
    </tr>
    <tr>
      <td>18</td>
      <td>1, Collectie</td>
      <td>Definitief manco</td>
      <td>Definitely missing</td>
    </tr>
    <tr>
      <td>19</td>
      <td>1, Collectie</td>
      <td>Zending afgekeurd</td>
      <td>Shipment rejected</td>
    </tr>
    <tr>
      <td>5</td>
      <td>2, Sortering</td>
      <td>Zending gesorteerd</td>
      <td>Shipment sorted</td>
    </tr>
    <tr>
      <td>6</td>
      <td>2, Sortering</td>
      <td>Zending niet gesorteerd</td>
      <td>Shipment not sorted</td>
    </tr>
    <tr>
      <td>16</td>
      <td>2, Sortering</td>
      <td>Manco sortering</td>
      <td>Missing in sorting</td>
    </tr>
    <tr>
      <td>21</td>
      <td>2, Sortering</td>
      <td>Zending in voorraad</td>
      <td>Shipment in storage</td>
    </tr>
    <tr>
      <td>7</td>
      <td>3, Distributie</td>
      <td>Zending in distributieproces</td>
      <td>Shipment out for delivery</td>
    </tr>
    <tr>
      <td>8</td>
      <td>3, Distributie</td>
      <td>Zending niet afgeleverd</td>
      <td>Shipment not delivered</td>
    </tr>
    <tr>
      <td>9</td>
      <td>3, Distributie</td>
      <td>Zending bij douane</td>
      <td>Shipment at customs</td>
    </tr>
    <tr>
      <td>17</td>
      <td>3, Distributie</td>
      <td>Manco distributie</td>
      <td>Missing in distribution</td>
    </tr>
    <tr>
      <td>20</td>
      <td>3, Distributie</td>
      <td>Zending in inklaringsproces</td>
      <td>Shipment in clearance process</td>
    </tr>
    <tr>
      <td>11</td>
      <td>4, Afgeleverd</td>
      <td>Zending afgeleverd</td>
      <td>Shipment delivered</td>
    </tr>
    <tr>
      <td>12</td>
      <td>4, Afgeleverd</td>
      <td>Zending beschikbaar op afhaallocatie</td>
      <td>Shipment at pick-up location</td>
    </tr>
    <tr>
      <td>22</td>
      <td>4, Afgeleverd</td>
      <td>Zending afgehaald van Postkantoor</td>
      <td>Shipment picked up from post office</td>
    </tr>
    <tr>
      <td>23</td>
      <td>4, Afgeleverd</td>
      <td>Afhaalopdracht gecollecteerd</td>
      <td>Parcel collected</td>
    </tr>
    <tr>
      <td>99</td>
      <td>99, Niet van toepassing</td>
      <td>Niet van toepassing</td>
      <td>Not applicable</td>
    </tr>
  </tbody>
</table>

# Event codes

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-8fdo{background-color:#CFC;text-align:left;vertical-align:top}
.tg .tg-eb4o{background-color:#E6B8B7;text-align:left;vertical-align:top}
.tg .tg-1wv6{background-color:#808080;color:#FFF;text-align:left;vertical-align:top}
.tg .tg-mmlj{background-color:#FABF8F;text-align:left;vertical-align:top}
.tg .tg-145f{background-color:#FF9;text-align:left;vertical-align:top}
.tg .tg-0lax{text-align:left;vertical-align:top}
.tg .tg-4c9j{background-color:#8DB4E2;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <thead>
    <tr>
      <th>Event</th>
      <th>Description NL ext</th>
      <th>Description EN ext</th>
      <th>Status option</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="tg-0lax">A01</td>
      <td class="tg-0lax">Pakket is nog niet door PostNL ontvangen of verwerkt</td>
      <td class="tg-0lax">Shipment expected, but not yet arrived at PostNL</td>
      <td class="tg-mmlj">01, Zending voorgemeld</td>
    </tr>
    <tr>
      <td class="tg-0lax">A10</td>
      <td class="tg-0lax">Verzender heeft retourlabel gegenereerd</td>
      <td class="tg-0lax">Sender has generated return label</td>
      <td class="tg-mmlj">01, Zending voorgemeld</td>
    </tr>
    <tr>
      <td class="tg-0lax">A71</td>
      <td class="tg-0lax">Zending aangemeld</td>
      <td class="tg-0lax">Shipment registered</td>
      <td class="tg-mmlj">01, Zending voorgemeld</td>
    </tr>
    <tr>
      <td class="tg-0lax">F01</td>
      <td class="tg-0lax">Afhaalzending wordt opgehaald</td>
      <td class="tg-0lax">Pick-up shipment will be collected</td>
      <td class="tg-mmlj">01, Zending voorgemeld</td>
    </tr>
    <tr>
      <td class="tg-0lax">J93</td>
      <td class="tg-0lax">Voorgemelde zending gedeeltelijk niet aangetroffen</td>
      <td class="tg-0lax">Pre-alerted shipment partially not found</td>
      <td class="tg-mmlj">01, Zending voorgemeld</td>
    </tr>
    <tr>
      <td class="tg-0lax">M03</td>
      <td class="tg-0lax">Geldigheidsduur label verstreken</td>
      <td class="tg-0lax">Period of validity label expired</td>
      <td class="tg-mmlj">01, Zending voorgemeld</td>
    </tr>
    <tr>
      <td class="tg-0lax">X80</td>
      <td class="tg-0lax">Afhaalopdracht ontvangen</td>
      <td class="tg-0lax">Collection order received</td>
      <td class="tg-mmlj">01, Zending voorgemeld</td>
    </tr>
    <tr>
      <td class="tg-0lax">X81</td>
      <td class="tg-0lax">Retourzending ontvangen in land van bestemming</td>
      <td class="tg-0lax">Return shipment received in country of destination</td>
      <td class="tg-mmlj">01, Zending voorgemeld</td>
    </tr>
    <tr>
      <td class="tg-0lax">B01</td>
      <td class="tg-0lax">Zending is ontvangen door PostNL</td>
      <td class="tg-0lax">Shipment received by PostNL</td>
      <td class="tg-mmlj">02, Zending in ontvangst genomen</td>
    </tr>
    <tr>
      <td class="tg-0lax">X40</td>
      <td class="tg-0lax">Zending ontvangen op PostNL-punt</td>
      <td class="tg-0lax">Shipment received at PostNL outlet</td>
      <td class="tg-mmlj">02, Zending in ontvangst genomen</td>
    </tr>
    <tr>
      <td class="tg-0lax">B04</td>
      <td class="tg-0lax">Zending is afgehaald door PostNL</td>
      <td class="tg-0lax">Shipment collected by PostNL</td>
      <td class="tg-mmlj">03, Zending afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z80</td>
      <td class="tg-0lax">Yes! Je zending is opgehaald bij een ophaalpunt</td>
      <td class="tg-0lax">Yes! Your shipment has been picked up at a collection point</td>
      <td class="tg-mmlj">03, Zending afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D02</td>
      <td class="tg-0lax">Zending niet afgehaald, adres onjuist</td>
      <td class="tg-0lax">Shipment not collected; incorrect address</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D03</td>
      <td class="tg-0lax">Afhaalzending niet opgehaald, niemand op adres aanwezig</td>
      <td class="tg-0lax">Collection shipment not collected, no one present at address</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D04</td>
      <td class="tg-0lax">Zending niet opgehaald, onjuist adres</td>
      <td class="tg-0lax">Shipment not collected; incorrect address</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D05</td>
      <td class="tg-0lax">Er was geen zending om af te halen</td>
      <td class="tg-0lax">There was no shipment to collect</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D06</td>
      <td class="tg-0lax">Afhaalzending niet opgehaald, zending geen (correct) label</td>
      <td class="tg-0lax">Collection shipment not collected, shipment incorrectly/not labelled</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D07</td>
      <td class="tg-0lax">Afhaalzending niet opgehaald, zending niet goed verpakt</td>
      <td class="tg-0lax">Collection shipment not collected, shipment not properly packed</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D09</td>
      <td class="tg-0lax">Afhaalzending niet opgehaald, geen gehoor</td>
      <td class="tg-0lax">Collection shipment not collected, no answer</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D40</td>
      <td class="tg-0lax">Afhaalzending niet opgehaald</td>
      <td class="tg-0lax">Collection shipment not collected</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">D41</td>
      <td class="tg-0lax">Afhaalopdracht geannuleerd</td>
      <td class="tg-0lax">Pick-up order cancelled</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">H31</td>
      <td class="tg-0lax">Verzender heeft de zendingsopdracht geannuleerd</td>
      <td class="tg-0lax">Sender has cancelled the shipment order</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">X42</td>
      <td class="tg-0lax">Zending geweigerd bij PostNL-punt, te groot/te zwaar</td>
      <td class="tg-0lax">Shipment refused at PostNL outlet, too large/too heavy</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">X43</td>
      <td class="tg-0lax">Zending geweigerd bij PostNL-punt, niet goed verpakt</td>
      <td class="tg-0lax">Shipment refused at PostNL outlet, insufficient packaging</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y80</td>
      <td class="tg-0lax">We hebben je gemist, we komen nog een keer</td>
      <td class="tg-0lax">We missed you; we’ll try again</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y81</td>
      <td class="tg-0lax">Afhaalopdracht mislukt, geen nieuwe poging</td>
      <td class="tg-0lax">Pick-up order unsuccessful, no new attempt</td>
      <td class="tg-mmlj">04, Zending niet afgehaald</td>
    </tr>
    <tr>
      <td class="tg-0lax">A08</td>
      <td class="tg-0lax">Keuze van ontvanger: bezorgen bij buren</td>
      <td class="tg-0lax">Recipient’s choice: deliver to neighbour</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A09</td>
      <td class="tg-0lax">Keuze van ontvanger: bezorgen op afhaallocatie</td>
      <td class="tg-0lax">Recipient’s choice: deliver to pick-up location</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A11</td>
      <td class="tg-0lax">Keuze van ontvanger: bezorgen bij willekeurige buren</td>
      <td class="tg-0lax">Recipient’s choice: deliver to random neighbour</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A12</td>
      <td class="tg-0lax">Keuze van ontvanger: bezorgen op andere dag</td>
      <td class="tg-0lax">Recipient’s choice: deliver on a different day</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A13</td>
      <td class="tg-0lax">Keuze van ontvanger: bezorgen in een ander dagdeel</td>
      <td class="tg-0lax">Recipient’s choice: deliver on a different part of the day</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A27</td>
      <td class="tg-0lax">Zending wordt afgeleverd bij de pakketautomaat</td>
      <td class="tg-0lax">Shipment will be delivered to the parcel locker</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A28</td>
      <td class="tg-0lax">Vanaf 09.00 uur af te halen bij PostNL-punt</td>
      <td class="tg-0lax">To be collected at PostNL outlet from 9:00am</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A29</td>
      <td class="tg-0lax">Zending wordt afgeleverd in de avond op een ander adres</td>
      <td class="tg-0lax">Shipment will be delivered in the evening to another address</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A30</td>
      <td class="tg-0lax">Zending wordt afgeleverd op een ander adres</td>
      <td class="tg-0lax">Shipment will be delivered to a different address</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A31</td>
      <td class="tg-0lax">Zending wordt afgeleverd in de avond bij buren</td>
      <td class="tg-0lax">Shipment will be delivered in the evening to a neighbour</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A32</td>
      <td class="tg-0lax">Zending wordt bezorgd in de avond op een andere dag</td>
      <td class="tg-0lax">Shipment will be delivered in the evening on another day</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A34</td>
      <td class="tg-0lax">Bezorging gewijzigd naar een PostNL-punt</td>
      <td class="tg-0lax">Delivery changed to a PostNL outlet</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A35</td>
      <td class="tg-0lax">Bezorging gewijzigd naar een andere dag</td>
      <td class="tg-0lax">Delivery changed to another day</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A42</td>
      <td class="tg-0lax">De bezorgdatum van de zending is aangepast</td>
      <td class="tg-0lax">Delivery date of shipment changed</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A43</td>
      <td class="tg-0lax">E-mail is verzonden met uitnodiging voor 2de bezorgpoging</td>
      <td class="tg-0lax">E-mail with invitation for 2nd delivery attempt sent</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A99</td>
      <td class="tg-0lax">Zending wordt bezorgd op PostNL-punt</td>
      <td class="tg-0lax">Shipment will be delivered to a PostNL outlet</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J01</td>
      <td class="tg-0lax">Zending is gesorteerd</td>
      <td class="tg-0lax">Shipment has been sorted</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J06</td>
      <td class="tg-0lax">Zending gesorteerd in sorteercentrum</td>
      <td class="tg-0lax">Shipment sorted in sorting centre</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J07</td>
      <td class="tg-0lax">Gesloten: aflevering uitgesteld tot volgende werkdag</td>
      <td class="tg-0lax">Closed: delivery postponed until the following working day</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J09</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J10</td>
      <td class="tg-0lax">Zending is gesorteerd</td>
      <td class="tg-0lax">Shipment has been sorted</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J14</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J16</td>
      <td class="tg-0lax">Bezorgadres onbereikbaar, nieuwe poging volgt</td>
      <td class="tg-0lax">Delivery address inaccessible, new attempt to follow</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J17</td>
      <td class="tg-0lax">Aflevering uitgesteld i.v.m. gesloten verklaring</td>
      <td class="tg-0lax">Delivery postponed due to ‘closed’ notification</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J22</td>
      <td class="tg-0lax">Uitstel van aflevering vanwege incomplete multicollozending</td>
      <td class="tg-0lax">Delivery postponed because of incomplete multi-parcel shipment</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J24</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J26</td>
      <td class="tg-0lax">Aflevering uitgesteld tot volgende werkdag</td>
      <td class="tg-0lax">Delivery postponed until the following working day</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J27</td>
      <td class="tg-0lax">Zending gesorteerd door depot</td>
      <td class="tg-0lax">Shipment sorted by the depot</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J28</td>
      <td class="tg-0lax">Vanwege formaat wordt zending bezorgd door PostNL Extra@Home</td>
      <td class="tg-0lax">Due to size, shipment will be delivered by PostNL Extra@Home</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J33</td>
      <td class="tg-0lax">Herstelprocedure ivm onjuiste adressering</td>
      <td class="tg-0lax">Recovery procedure for incorrect address</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J36</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J61</td>
      <td class="tg-0lax">Zending is gesorteerd</td>
      <td class="tg-0lax">Shipment has been sorted</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J90</td>
      <td class="tg-0lax">Zending wordt geleverd op een aangegeven gewenste datum</td>
      <td class="tg-0lax">Shipment will be delivered on an indicated desired date</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q12</td>
      <td class="tg-0lax">Pakket verzonden naar land van bestemming</td>
      <td class="tg-0lax">Shipment sent to country of destination</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q13</td>
      <td class="tg-0lax">Pakket op transport gezet</td>
      <td class="tg-0lax">Parcel placed on transport</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">R01</td>
      <td class="tg-0lax">Zending is gesorteerd</td>
      <td class="tg-0lax">Shipment has been sorted</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">R06</td>
      <td class="tg-0lax">Zending is geannuleerd; neem contact op met de afzender</td>
      <td class="tg-0lax">Shipment has been cancelled. Please contact the sender</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X01</td>
      <td class="tg-0lax">Goed nieuws! Je zending is de grens over</td>
      <td class="tg-0lax">Good news! Your parcel has crossed the border</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X02</td>
      <td class="tg-0lax">Yes! Je zending is aangekomen in het land van bestemming</td>
      <td class="tg-0lax">Yes! Your shipment has arrived in the destination country</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X07</td>
      <td class="tg-0lax">Zending is gesorteerd in land van bestemming</td>
      <td class="tg-0lax">Shipment sorted in country of destination</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X08</td>
      <td class="tg-0lax">Je zending ligt op een sorteercentrum in land van bestemming</td>
      <td class="tg-0lax">Your parcel's at a sorting centre in the destination country</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X11</td>
      <td class="tg-0lax">Antwoord met informatie voor import aangifte ontvangen</td>
      <td class="tg-0lax">Answer received with information for import declaration</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X14</td>
      <td class="tg-0lax">Zending in sorteercentrum in land van bestemming</td>
      <td class="tg-0lax">Shipment in sorting centre in country of destination</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X17</td>
      <td class="tg-0lax">Zending gewogen en gewicht bepaald</td>
      <td class="tg-0lax">Shipment weighed and weight determined at IMEC.</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X20</td>
      <td class="tg-0lax">Retourzending ontvangen in distributiecentrum buitenland</td>
      <td class="tg-0lax">Return shipment received in distribution centre abroad</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X21</td>
      <td class="tg-0lax">Retourzending ontvangen in distributiecentrum</td>
      <td class="tg-0lax">Return shipment received in distribution centre</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X22</td>
      <td class="tg-0lax">Zending uit buitenland komt retour</td>
      <td class="tg-0lax">International shipment returned</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X50</td>
      <td class="tg-0lax">Zending in sorteercentrum</td>
      <td class="tg-0lax">Shipment in sorting centre</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X51</td>
      <td class="tg-0lax">Zending is gesorteerd</td>
      <td class="tg-0lax">Shipment has been sorted</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X68</td>
      <td class="tg-0lax">Pakket weer terug in PostNL-proces</td>
      <td class="tg-0lax">Parcel back in PostNL process</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y23</td>
      <td class="tg-0lax">Adres is gecorrigeerd, nieuwe bezorgpoging volgt</td>
      <td class="tg-0lax">Address corrected, new delivery attempt to follow</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y24</td>
      <td class="tg-0lax">Adres is gecorrigeerd, nieuwe bezorgpoging volgt</td>
      <td class="tg-0lax">Address corrected, new delivery attempt to follow</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y33</td>
      <td class="tg-0lax">Aflevering uitgesteld tot volgende werkdag</td>
      <td class="tg-0lax">Delivery postponed until the following working day</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y35</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y60</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y61</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y62</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">05, Zending gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">D08</td>
      <td class="tg-0lax">We hebben je gemist, we komen nog een keer</td>
      <td class="tg-0lax">We missed you; we’ll try again</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H10</td>
      <td class="tg-0lax">Retour, inhoud niet toegestaan</td>
      <td class="tg-0lax">Return, content not permitted</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K01</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K02</td>
      <td class="tg-0lax">Ontvanger is verhuisd. Zending doorgestuurd naar nieuw adres</td>
      <td class="tg-0lax">Recipient has moved. Shipment forwarded to new address</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K03</td>
      <td class="tg-0lax">Zending doorgestuurd naar door geadresseerde gekozen adres.</td>
      <td class="tg-0lax">Shipment forwarded to address chosen by addressee.</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K30</td>
      <td class="tg-0lax">Zending kan niet bezorgd worden; Neem contact op met klantenservice</td>
      <td class="tg-0lax">Shipment cannot be delivered</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K92</td>
      <td class="tg-0lax">Zending vernietigd</td>
      <td class="tg-0lax">Shipment destroyed</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">V01</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">V06</td>
      <td class="tg-0lax">Wegens  drukte is je zending&nbsp;&nbsp;&nbsp;vertraagd. Deze zal zo snel mogelijk worden bezorgd</td>
      <td class="tg-0lax">Your shipment has been delayed due to very high traffic. It will be&nbsp;&nbsp;&nbsp;delivered as soon as p</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y07</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">06, Zending niet gesorteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H32</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">H35</td>
      <td class="tg-0lax">Zending is beschadigd, gaat retour afzender</td>
      <td class="tg-0lax">Shipment is damaged, return to sender</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J05</td>
      <td class="tg-0lax">Bezorger is onderweg</td>
      <td class="tg-0lax">Driver is en route</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J08</td>
      <td class="tg-0lax">Bezorgen lukte niet, we proberen het nog een keer</td>
      <td class="tg-0lax">Delivery unsuccessful, we’ll try again</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J29</td>
      <td class="tg-0lax">Zending paste niet door brievenbus, we komen nog een keer</td>
      <td class="tg-0lax">Shipment does not fit through letterbox, we’ll try again</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J39</td>
      <td class="tg-0lax">Aflevering uitgesteld tot volgende werkdag  </td>
      <td class="tg-0lax">Delivery postponed until the following working day  </td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J41</td>
      <td class="tg-0lax">Zending niet toegestaan in de pakketautomaat</td>
      <td class="tg-0lax">Shipment not allowed in the parcel locker</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J42</td>
      <td class="tg-0lax">Zending past niet in de pakketautomaat</td>
      <td class="tg-0lax">Insufficient space in the parcel locker</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J45</td>
      <td class="tg-0lax">Op lijndienst naar distributie depot</td>
      <td class="tg-0lax">On liner service to distribution depot</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J47</td>
      <td class="tg-0lax">Zending niet opgehaald, gaat naar PostNL-punt</td>
      <td class="tg-0lax">Pickup window closed; shipment moved to PostNL pickup point</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J48</td>
      <td class="tg-0lax">Pakket te groot om te bezorgen in de pakketautomaat</td>
      <td class="tg-0lax">Parcel too large for delivery in the parcel locker</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J55</td>
      <td class="tg-0lax">Bezorger is onderweg naar PostNL-punt</td>
      <td class="tg-0lax">Driver is en route to PostNL outlet</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J94</td>
      <td class="tg-0lax">Vrachtzending niet afgeleverd, geadresseerde afwezig</td>
      <td class="tg-0lax">Freight shipment not delivered; addressee absent</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">J95</td>
      <td class="tg-0lax">Uitgesteld, gescand op depot</td>
      <td class="tg-0lax">Postponed, scanned at depot</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">K14</td>
      <td class="tg-0lax">Wij hebben je gemist, we komen nog een keer</td>
      <td class="tg-0lax">We missed you; we’ll try again</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">K15</td>
      <td class="tg-0lax">Fout bij bezorging zending. Nadere informatie volgt</td>
      <td class="tg-0lax">Error during shipment delivery. More information to follow</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">K70</td>
      <td class="tg-0lax">Bezorgen lukte niet, zending gaat naar PostNL-punt</td>
      <td class="tg-0lax">Delivery unsuccessful, shipment will go to PostNL outlet</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q15</td>
      <td class="tg-0lax">Zending is onderweg</td>
      <td class="tg-0lax">Shipment is en route</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">S05</td>
      <td class="tg-0lax">Zending is onderweg</td>
      <td class="tg-0lax">Shipment is en route</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">T02</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">X04</td>
      <td class="tg-0lax">De douane in het land van bestemming heeft je zending goedgekeurd</td>
      <td class="tg-0lax">Customs in the destination country has approved your parcel</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">X06</td>
      <td class="tg-0lax">Je zending is onderweg naar de ontvanger</td>
      <td class="tg-0lax">Your shipment is on its way to the recipient</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">X19</td>
      <td class="tg-0lax">Zending verzonden naar land van bestemming</td>
      <td class="tg-0lax">Shipment sent to country of destination</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">X55</td>
      <td class="tg-0lax">Bezorger is onderweg</td>
      <td class="tg-0lax">Driver is en route</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y05</td>
      <td class="tg-0lax">Je zending is onderweg naar de ontvanger</td>
      <td class="tg-0lax">Your shipment is on its way to the recipient</td>
      <td class="tg-8fdo">07, Zending in distributieproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">H01</td>
      <td class="tg-0lax">Geweigerd bij bezorging, zending gaat retour afzender</td>
      <td class="tg-0lax">Refused at delivery; return shipment to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H02</td>
      <td class="tg-0lax">Adres onjuist, zending gaat retour afzender</td>
      <td class="tg-0lax">Incorrect address; return shipment to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H03</td>
      <td class="tg-0lax">Zending niet afgehaald, gaat retour afzender</td>
      <td class="tg-0lax">Shipment not collected, return to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H04</td>
      <td class="tg-0lax">Zending is beschadigd, gaat retour afzender</td>
      <td class="tg-0lax">Shipment is damaged, return to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H05</td>
      <td class="tg-0lax">We hebben je gemist, zending gaat retour afzender</td>
      <td class="tg-0lax">We missed you; shipment returned to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H07</td>
      <td class="tg-0lax">We hebben je gemist, zending gaat retour afzender</td>
      <td class="tg-0lax">We missed you; shipment returned to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H08</td>
      <td class="tg-0lax">Aflevercode of legitimatie onjuist, zending retour afzender</td>
      <td class="tg-0lax">Incorrect delivery code or ID, return shipment to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H09</td>
      <td class="tg-0lax">Zending niet compleet, retour afzender</td>
      <td class="tg-0lax">Shipment incomplete, return to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H12</td>
      <td class="tg-0lax">Zending retour afzender, geadresseerde onjuist</td>
      <td class="tg-0lax">Shipment returned to sender, addressee incorrect</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H20</td>
      <td class="tg-0lax">Zending retour afzender</td>
      <td class="tg-0lax">Shipment returned to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H22</td>
      <td class="tg-0lax">Zending op verzoek van afzender retour gestuurd</td>
      <td class="tg-0lax">Shipment returned on request of sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H24</td>
      <td class="tg-0lax">Retour gestuurd door afhaallocatie op verzoek van ontvanger</td>
      <td class="tg-0lax">Returned by pick-up location on recipient’s request</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H34</td>
      <td class="tg-0lax">Zending niet afgeleverd</td>
      <td class="tg-0lax">Shipment not delivered</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H36</td>
      <td class="tg-0lax">Zending niet bezorgd, adres onjuist</td>
      <td class="tg-0lax">Shipment not delivered; incorrect address</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H38</td>
      <td class="tg-0lax">Geweigerd bij bezorging, zending gaat retour afzender</td>
      <td class="tg-0lax">Refused at delivery; return shipment to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H51</td>
      <td class="tg-0lax">Zending niet afgeleverd, geen brievenbus. Retour afzender.</td>
      <td class="tg-0lax">Shipment not delivered, no letterbox. Return to sender.</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H52</td>
      <td class="tg-0lax">Zending niet afgeleverd, past niet. Retour afzender.</td>
      <td class="tg-0lax">Shipment not delivered, does not fit. Return to sender.</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J92</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K16</td>
      <td class="tg-0lax">Bezorgadres onbereikbaar, nieuwe poging volgt</td>
      <td class="tg-0lax">Shipment not delivered, address long term unreachable</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K41</td>
      <td class="tg-0lax">Rembours zend. niet afgeleverd, ontvanger kan niet betalen</td>
      <td class="tg-0lax">Cash on Delivery shipment not delivered, recipient cannot pay</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K43</td>
      <td class="tg-0lax">Zending wordt geretourneerd</td>
      <td class="tg-0lax">Shipment will be returned</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y01</td>
      <td class="tg-0lax">Zending niet bezorgd, adres incorrect</td>
      <td class="tg-0lax">Shipment not delivered; incorrect address</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y02</td>
      <td class="tg-0lax">We hebben je gemist, zending niet bezorgd</td>
      <td class="tg-0lax">We missed you; shipment not delivered</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y03</td>
      <td class="tg-0lax">Zending geweigerd door geadresseerde</td>
      <td class="tg-0lax">Shipment refused by addressee</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y04</td>
      <td class="tg-0lax">Zending beschadigd</td>
      <td class="tg-0lax">Shipment damaged</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y08</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y09</td>
      <td class="tg-0lax">Contact met geadresseerde vanwege incorrect afleveradres</td>
      <td class="tg-0lax">Contact addressee due to incorrect delivery address</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y10</td>
      <td class="tg-0lax">We hebben je gemist, we komen nog een keer</td>
      <td class="tg-0lax">We missed you; we’ll try again</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y11</td>
      <td class="tg-0lax">Zending beschadigd, contact gezocht met ontvanger</td>
      <td class="tg-0lax">Shipment damaged, attempt made to contact recipient</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y12</td>
      <td class="tg-0lax">Adres incorrect, PostNL neemt contact op met afzender</td>
      <td class="tg-0lax">Address incorrect, PostNL will contact sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y13</td>
      <td class="tg-0lax">Zending geweigerd, PostNL zoekt contact met afzender</td>
      <td class="tg-0lax">Shipment refused, PostNL contacting sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y14</td>
      <td class="tg-0lax">Zending beschadigd</td>
      <td class="tg-0lax">Shipment damaged</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y15</td>
      <td class="tg-0lax">Zending niet bezorgd, contact met afzender</td>
      <td class="tg-0lax">Shipment not delivered, sender contacted</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y16</td>
      <td class="tg-0lax">Adres incorrect, zending retour afzender</td>
      <td class="tg-0lax">Address incorrect, return shipment to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y17</td>
      <td class="tg-0lax">Zending niet bezorgd, adres incorrect</td>
      <td class="tg-0lax">Shipment not delivered; incorrect address</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y18</td>
      <td class="tg-0lax">Zending is beschadigd, zending retour afzender</td>
      <td class="tg-0lax">Shipment is damaged, return shipment to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y19</td>
      <td class="tg-0lax">Zending bevat verboden artikel, zending retour afzender</td>
      <td class="tg-0lax">Shipment contains prohibited item, return shipment to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y20</td>
      <td class="tg-0lax">Zending niet afgehaald, gaat retour afzender</td>
      <td class="tg-0lax">Shipment not collected, return to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y21</td>
      <td class="tg-0lax">Zending retour afzender</td>
      <td class="tg-0lax">Shipment returned to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y22</td>
      <td class="tg-0lax">Zending niet afgeleverd, geadresseerde verhuisd</td>
      <td class="tg-0lax">Shipment not delivered, addressee relocated</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y30</td>
      <td class="tg-0lax">Zending is niet afgeleverd i.v.m. onjuiste postcode</td>
      <td class="tg-0lax">Shipment not delivered due to incorrect postcode</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y31</td>
      <td class="tg-0lax">Zending niet bezorgd, ontbrekende postcode</td>
      <td class="tg-0lax">Shipment not delivered, missing postcode</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y32</td>
      <td class="tg-0lax">Zending niet bezorgd, onbekend adres</td>
      <td class="tg-0lax">Shipment not delivered, address unknown</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y36</td>
      <td class="tg-0lax">Zending niet afgeleverd: identificatie ontvanger ontbreekt</td>
      <td class="tg-0lax">Shipment not delivered: recipient identification missing</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y38</td>
      <td class="tg-0lax">Zending niet afgeleverd: pakket naar depot bestemmingsland</td>
      <td class="tg-0lax">Shipment not delivered: parcel sent to depot in destination country</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y39</td>
      <td class="tg-0lax">Contact met ontvanger om een afspraak te plannen. </td>
      <td class="tg-0lax">Contact recipient to arrange an appointment. </td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y40</td>
      <td class="tg-0lax">We hebben je gemist, zending gaat retour afzender</td>
      <td class="tg-0lax">We missed you; shipment returned to sender</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y41</td>
      <td class="tg-0lax">Zending is niet afgeleverd. Toegangscode locatie ontbreekt</td>
      <td class="tg-0lax">Shipment not delivered. Location access code is missing</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y42</td>
      <td class="tg-0lax">Zending is niet afgeleverd, geadresseerde is onbereikbaar</td>
      <td class="tg-0lax">Shipment not delivered, addressee unavailable</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y43</td>
      <td class="tg-0lax">Zending vertraagd wegens gesloten locatie geadresseerde</td>
      <td class="tg-0lax">Shipment delayed as addressee location is closed</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y44</td>
      <td class="tg-0lax">Zending door ontvanger geweigerd wegens beschadiging. </td>
      <td class="tg-0lax">Shipment refused by recipient due to damage. </td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y50</td>
      <td class="tg-0lax">Zending geweigerd; onvolledig</td>
      <td class="tg-0lax">Shipment refused, incomplete</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y71</td>
      <td class="tg-0lax">Zending is vermist</td>
      <td class="tg-0lax">Shipment missing</td>
      <td class="tg-8fdo">08, Zending niet afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J59</td>
      <td class="tg-0lax">Pakket wordt vandaag toch nog via een koerier bij je bezorgd</td>
      <td class="tg-0lax">Parcel will be delivered to you today by courier</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">X30</td>
      <td class="tg-0lax">Zending vertraagd in land van bestemming door aanvullend onderzoek bij&nbsp;&nbsp;&nbsp;inklaring</td>
      <td class="tg-0lax">Shipment delayed in destination country due to additional investigation&nbsp;&nbsp;&nbsp;at customs clea</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">X60</td>
      <td class="tg-0lax">Invoeraangifte ingediend door PostNL</td>
      <td class="tg-0lax">Import declaration submitted by PostNL</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">X61</td>
      <td class="tg-0lax">Invoeraangifte succesvol afgerond</td>
      <td class="tg-0lax">Import declaration completed successfully</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">X62</td>
      <td class="tg-0lax">Aanvullende aangifte is ingediend</td>
      <td class="tg-0lax">Additional declaration has been submitted</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">X63</td>
      <td class="tg-0lax">Zending vertraagd vanwege steekproefcontrole bij inklaring</td>
      <td class="tg-0lax">Shipment delayed due to sample check at customs clearance</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">X64</td>
      <td class="tg-0lax">Zending vertraagd vanwege steekproefcontrole bij inklaring</td>
      <td class="tg-0lax">Shipment delayed due to sample check at customs clearance</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">X65</td>
      <td class="tg-0lax">Aanvullende aangifte succesvol afgerond bij douane</td>
      <td class="tg-0lax">Additional customs declaration completed successfully</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">X66</td>
      <td class="tg-0lax">Het aangifteproces  van de&nbsp;&nbsp;&nbsp;zending is stopgezet</td>
      <td class="tg-0lax">Shipment declaration process has been stopped</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y25</td>
      <td class="tg-0lax">De zending ligt bij de douane in het land van bestemming voor verdere&nbsp;&nbsp;&nbsp;afhandeling</td>
      <td class="tg-0lax">The shipment is with the customs authorities in the destination country&nbsp;&nbsp;&nbsp;for further proc</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y29</td>
      <td class="tg-0lax">De zending is vernietigd namens de douane in land van bestemming</td>
      <td class="tg-0lax">The shipment has been destroyed on behalf of customs in the destination&nbsp;&nbsp;&nbsp;country</td>
      <td class="tg-8fdo">09, Zending bij douane</td>
    </tr>
    <tr>
      <td class="tg-0lax">I01</td>
      <td class="tg-0lax">Zending is bezorgd</td>
      <td class="tg-0lax">Shipment delivered</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I03</td>
      <td class="tg-0lax">Zending is bezorgd</td>
      <td class="tg-0lax">Shipment delivered</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I05</td>
      <td class="tg-0lax">Zending is bezorgd in de brievenbus</td>
      <td class="tg-0lax">Shipment in letterbox</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I06</td>
      <td class="tg-0lax">Zending gesorteerd, wordt overgedragen aan geadresseerde</td>
      <td class="tg-0lax">Shipment sorted, will be transferred to addressee</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I07</td>
      <td class="tg-0lax">Retourzending gesorteerd, wordt overgedragen aan afzender</td>
      <td class="tg-0lax">Return shipment sorted, will be transferred to sender</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I09</td>
      <td class="tg-0lax">Zending afgeleverd in pakketkluis</td>
      <td class="tg-0lax">Shipment delivered in personal parcel locker</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I10</td>
      <td class="tg-0lax">Zending is bezorgd bij de buren</td>
      <td class="tg-0lax">Shipment delivered to neighbour</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I11</td>
      <td class="tg-0lax">Zending is bezorgd in de brievenbus</td>
      <td class="tg-0lax">Shipment in letterbox</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I12</td>
      <td class="tg-0lax">Zending is bezorgd op de afgesproken plek</td>
      <td class="tg-0lax">Shipment delivered to indicated location</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I22</td>
      <td class="tg-0lax">Zending is afgehaald bij PostNL-punt</td>
      <td class="tg-0lax">Shipment collected at PostNL outlet</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I23</td>
      <td class="tg-0lax">Zending is overhandigd aan ontvanger</td>
      <td class="tg-0lax">Shipment has been handed over to recipient</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J23</td>
      <td class="tg-0lax">Zending kan worden afgehaald bij de pakketautomaat</td>
      <td class="tg-0lax">Shipment can be collected at the parcel locker</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J63</td>
      <td class="tg-0lax">Retourzending afgeleverd</td>
      <td class="tg-0lax">Return shipment delivered</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">J91</td>
      <td class="tg-0lax">Gedeeltelijk manco aangeleverde zending afgeleverd</td>
      <td class="tg-0lax">Partially-defective shipment delivered</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">K91</td>
      <td class="tg-0lax">In opslag i.v.m. calamiteit tot nader order</td>
      <td class="tg-0lax">In storage because of closed return address – coronavirus measure</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">X24</td>
      <td class="tg-0lax">Zending retour gestuurd naar zakelijke postbushouder in het buitenland.</td>
      <td class="tg-0lax">Shipment returned to business PO Box holder abroad</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y26</td>
      <td class="tg-0lax">Zending af te halen bij postbus</td>
      <td class="tg-0lax">Shipment to be collected at PO Box</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z01</td>
      <td class="tg-0lax">Yes! Je zending is bezorgd bij de ontvanger</td>
      <td class="tg-0lax">Yes! Your shipment has been delivered to the recipient</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z02</td>
      <td class="tg-0lax">Yes! Je zending is bezorgd bij de ontvanger</td>
      <td class="tg-0lax">Yes! Your shipment has been delivered to the recipient</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z03</td>
      <td class="tg-0lax">Yes! Je zending is bezorgd bij de ontvanger</td>
      <td class="tg-0lax">Yes! Your shipment has been delivered to the recipient</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z04</td>
      <td class="tg-0lax">Yes! Je zending is bezorgd bij de ontvanger</td>
      <td class="tg-0lax">Yes! Your shipment has been delivered to the recipient</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z05</td>
      <td class="tg-0lax">Je zending is bezorgd bij buren in het land van bestemming</td>
      <td class="tg-0lax">Parcel was delivered to neighbours in destination country</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z06</td>
      <td class="tg-0lax">Yes! Je zending is opgehaald bij een ophaalpunt</td>
      <td class="tg-0lax">Yes! Your shipment has been picked up at a collection point</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z08</td>
      <td class="tg-0lax">Yes! Je zending is bezorgd bij de ontvanger</td>
      <td class="tg-0lax">Yes! Your shipment has been delivered to the recipient</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">Z09</td>
      <td class="tg-0lax">Je zending is bezorgd op de veilige locatie van je ontvanger</td>
      <td class="tg-0lax">Your parcel has been delivered to recipient's safe location</td>
      <td class="tg-4c9j">11, Zending afgeleverd</td>
    </tr>
    <tr>
      <td class="tg-0lax">I08</td>
      <td class="tg-0lax">Zending beschikbaar op PostNL-punt</td>
      <td class="tg-0lax">Shipment available at PostNL outlet</td>
      <td class="tg-4c9j">12, Zending beschikbaar op afhaallocatie</td>
    </tr>
    <tr>
      <td class="tg-0lax">J02</td>
      <td class="tg-0lax">Pakket ligt voor je klaar op PostNL-punt</td>
      <td class="tg-0lax">Shipment to be collected at PostNL outlet</td>
      <td class="tg-4c9j">12, Zending beschikbaar op afhaallocatie</td>
    </tr>
    <tr>
      <td class="tg-0lax">J12</td>
      <td class="tg-0lax">Pakket ligt voor je klaar op PostNL-punt</td>
      <td class="tg-0lax">Shipment to be collected at PostNL outlet</td>
      <td class="tg-4c9j">12, Zending beschikbaar op afhaallocatie</td>
    </tr>
    <tr>
      <td class="tg-0lax">J23</td>
      <td class="tg-0lax">Zending kan worden afgehaald bij de pakketautomaat</td>
      <td class="tg-0lax">Shipment can be picked up at the parcel machine</td>
      <td class="tg-4c9j">12, Zending beschikbaar op afhaallocatie</td>
    </tr>
    <tr>
      <td class="tg-0lax">J52</td>
      <td class="tg-0lax">Zending af te halen bij postbus-locatie</td>
      <td class="tg-0lax">Shipment to be collected at PO Box location</td>
      <td class="tg-4c9j">12, Zending beschikbaar op afhaallocatie</td>
    </tr>
    <tr>
      <td class="tg-0lax">X05</td>
      <td class="tg-0lax">Zending af te halen bij afhaallocatie</td>
      <td class="tg-0lax">Shipment to be collected at pick-up location</td>
      <td class="tg-4c9j">12, Zending beschikbaar op afhaallocatie</td>
    </tr>
    <tr>
      <td class="tg-0lax">A20</td>
      <td class="tg-0lax">Verzoek tot betaling kosten voor zending verstuurd</td>
      <td class="tg-0lax">Request for payment of shipment costs sent</td>
      <td class="tg-mmlj">13, Voorgemeld: nog niet aangenomen</td>
    </tr>
    <tr>
      <td class="tg-0lax">A21</td>
      <td class="tg-0lax">Je hebt betaald, we maken je pakket klaar voor bezorging</td>
      <td class="tg-0lax">Payment for shipment costs received</td>
      <td class="tg-mmlj">13, Voorgemeld: nog niet aangenomen</td>
    </tr>
    <tr>
      <td class="tg-0lax">A22</td>
      <td class="tg-0lax">Verzoek tot betaling geweigerd</td>
      <td class="tg-0lax">Request for payment refused</td>
      <td class="tg-mmlj">13, Voorgemeld: nog niet aangenomen</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q02</td>
      <td class="tg-0lax">Transactie op PostNL-punt geannuleerd</td>
      <td class="tg-0lax">Transaction cancelled at PostNL outlet</td>
      <td class="tg-mmlj">13, Voorgemeld: nog niet aangenomen</td>
    </tr>
    <tr>
      <td class="tg-0lax">X03</td>
      <td class="tg-0lax">De douane in het land van bestemming checkt je zending</td>
      <td class="tg-0lax">Customs in the destination country is checking your shipment</td>
      <td class="tg-mmlj">13, Voorgemeld: nog niet aangenomen</td>
    </tr>
    <tr>
      <td class="tg-0lax">M01</td>
      <td class="tg-0lax">Pakket niet fysiek aangeboden aan PostNL</td>
      <td class="tg-0lax">Shipment not physically presented to PostNL</td>
      <td class="tg-mmlj">14, Voorgemeld: definitief niet aangenomen</td>
    </tr>
    <tr>
      <td class="tg-0lax">G03</td>
      <td class="tg-0lax">Door grote drukte duurt het wat langer dan normaal. We doen er alles&nbsp;&nbsp;&nbsp;aan om je pakket zo snel mogelijk te </td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-mmlj">15, Manco collectie</td>
    </tr>
    <tr>
      <td class="tg-0lax">G01</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">16, Manco sortering</td>
    </tr>
    <tr>
      <td class="tg-0lax">G02</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">16, Manco sortering</td>
    </tr>
    <tr>
      <td class="tg-0lax">G05</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">16, Manco sortering</td>
    </tr>
    <tr>
      <td class="tg-0lax">H23</td>
      <td class="tg-0lax">Geannuleerd door PostNL, geen bezorgafspraak kunnen maken.</td>
      <td class="tg-0lax">Cancelled by PostNL, no delivery appointment could be made.</td>
      <td class="tg-8fdo">17, Manco distributie</td>
    </tr>
    <tr>
      <td class="tg-0lax">K90</td>
      <td class="tg-0lax">Nog geen status bekend. Probeer later opnieuw.</td>
      <td class="tg-0lax">Status as yet unknown. Try again later.</td>
      <td class="tg-8fdo">17, Manco distributie</td>
    </tr>
    <tr>
      <td class="tg-0lax">F03</td>
      <td class="tg-0lax">Zending niet verwerkt vanwege ontbrekende verzendgegevens</td>
      <td class="tg-0lax">Shipment not processed because of missing shipment details</td>
      <td class="tg-mmlj">19, Zending afgekeurd</td>
    </tr>
    <tr>
      <td class="tg-0lax">F04</td>
      <td class="tg-0lax">Zending niet verwerkt vanwege ontbrekende verzendgegevens</td>
      <td class="tg-0lax">Shipment not processed because of missing shipment details</td>
      <td class="tg-mmlj">19, Zending afgekeurd</td>
    </tr>
    <tr>
      <td class="tg-0lax">F05</td>
      <td class="tg-0lax">Zending wordt niet verwerkt. Afhaalcontract ontbreekt</td>
      <td class="tg-0lax">Shipment will not be processed. Collection contract missing</td>
      <td class="tg-mmlj">19, Zending afgekeurd</td>
    </tr>
    <tr>
      <td class="tg-0lax">F06</td>
      <td class="tg-0lax">Zending wordt niet verwerkt. Postcode afhaaladres onbekend.</td>
      <td class="tg-0lax">Shipment will not be processed. Collection address post code unknown.</td>
      <td class="tg-mmlj">19, Zending afgekeurd</td>
    </tr>
    <tr>
      <td class="tg-0lax">F07</td>
      <td class="tg-0lax">Zending wordt niet verwerkt. Postcode bezorgadres onbekend.</td>
      <td class="tg-0lax">Shipment will not be processed. Delivery address post code unknown.</td>
      <td class="tg-mmlj">19, Zending afgekeurd</td>
    </tr>
    <tr>
      <td class="tg-0lax">F08</td>
      <td class="tg-0lax">Zending niet verwerkt. Afhaaldatum ligt in het verleden.</td>
      <td class="tg-0lax">Shipment not processed. Collection date is in the past.</td>
      <td class="tg-mmlj">19, Zending afgekeurd</td>
    </tr>
    <tr>
      <td class="tg-0lax">F10</td>
      <td class="tg-0lax">Zending wordt niet verwerkt. Afhaaldatum is geen werkdag.</td>
      <td class="tg-0lax">Shipment will not be processed. Collection date is not a working day.</td>
      <td class="tg-mmlj">19, Zending afgekeurd</td>
    </tr>
    <tr>
      <td class="tg-0lax">A76</td>
      <td class="tg-0lax">Zending aangekomen in Nederland</td>
      <td class="tg-0lax">Shipment arrived in the Netherlands</td>
      <td class="tg-8fdo">20, Zending in inklaringsproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">X10</td>
      <td class="tg-0lax">Er ontbreken pakket gegevens. Je ontvangt van ons een informatieverzoek</td>
      <td class="tg-0lax">Parcel details missing. You will receive an information request from us</td>
      <td class="tg-8fdo">20, Zending in inklaringsproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">X67</td>
      <td class="tg-0lax">Wacht op betaling importkosten</td>
      <td class="tg-0lax">Awaiting payment of import costs</td>
      <td class="tg-8fdo">20, Zending in inklaringsproces</td>
    </tr>
    <tr>
      <td class="tg-0lax">V02</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V03</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V04</td>
      <td class="tg-0lax">Bezorging is vertraagd, te laat aangeleverd bij PostNL</td>
      <td class="tg-0lax">Delivery delayed due to late delivery to PostNL</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V11</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V12</td>
      <td class="tg-0lax">Ontvangen door PostNL</td>
      <td class="tg-0lax">Received by PostNL</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V13</td>
      <td class="tg-0lax">Ontvangen door PostNL</td>
      <td class="tg-0lax">Received by PostNL</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V21</td>
      <td class="tg-0lax">Sorry, bezorgmoment is bijgewerkt</td>
      <td class="tg-0lax">Sorry, delivery time has been updated</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V22</td>
      <td class="tg-0lax">Zending is bij PostNL</td>
      <td class="tg-0lax">Shipment is at PostNL</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V23</td>
      <td class="tg-0lax">Ontvangen door PostNL</td>
      <td class="tg-0lax">Received by PostNL</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V31</td>
      <td class="tg-0lax">Ontvangen door PostNL, vertraagd</td>
      <td class="tg-0lax">Received by PostNL, delayed</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">V50</td>
      <td class="tg-0lax">Ontvangen door PostNL</td>
      <td class="tg-0lax">Received by PostNL</td>
      <td class="tg-145f">21, Zending in voorraad</td>
    </tr>
    <tr>
      <td class="tg-0lax">I02</td>
      <td class="tg-0lax">Zending is afgehaald bij PostNL-punt</td>
      <td class="tg-0lax">Shipment collected at PostNL outlet</td>
      <td class="tg-4c9j">22, Zending afgehaald van Postkantoor</td>
    </tr>
    <tr>
      <td class="tg-0lax">C01</td>
      <td class="tg-0lax">Zending is afgehaald door PostNL</td>
      <td class="tg-0lax">Shipment collected by PostNL</td>
      <td class="tg-4c9j">23, Afhaalopdracht gecollecteerd</td>
    </tr>
    <tr>
      <td class="tg-0lax">H16</td>
      <td class="tg-0lax">Bezorging niet gelukt, pakket gaat terug naar de afzender</td>
      <td class="tg-0lax">Shipment not delivered, address long unavailable. Return</td>
      <td class="tg-eb4o">27, Retour Onbestelbaar</td>
    </tr>
    <tr>
      <td class="tg-0lax">H25</td>
      <td class="tg-0lax">Bezorging niet mogelijk, pakket gaat terug naar afzender </td>
      <td class="tg-0lax">Shipment not delivered, location long term unreachable</td>
      <td class="tg-eb4o">27, Retour Onbestelbaar</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y37</td>
      <td class="tg-0lax">Zending niet afgeleverd: neem contact op met locale bezorger</td>
      <td class="tg-0lax">Shipment not delivered: contact local deliverer</td>
      <td class="tg-eb4o">28, Retour Foutieve aflevercode</td>
    </tr>
    <tr>
      <td class="tg-0lax">A72</td>
      <td class="tg-0lax">Zending is klaar voor transport naar Nederland</td>
      <td class="tg-0lax">Shipment is ready for transport to the Netherlands</td>
      <td class="tg-0lax">31, Zending klaar voor transport naar land van bestemming</td>
    </tr>
    <tr>
      <td class="tg-0lax">A74</td>
      <td class="tg-0lax">Zending is ontvangen door partner in land van verzending</td>
      <td class="tg-0lax">Shipment received by partner in country of shipment</td>
      <td class="tg-0lax">31, Zending klaar voor transport naar land van bestemming</td>
    </tr>
    <tr>
      <td class="tg-0lax">A75</td>
      <td class="tg-0lax">Zending is onderweg naar Nederland</td>
      <td class="tg-0lax">Shipment is en route to the Netherlands</td>
      <td class="tg-0lax">31, Zending klaar voor transport naar land van bestemming</td>
    </tr>
    <tr>
      <td class="tg-0lax">X15</td>
      <td class="tg-0lax">Zending gesorteerd in land van bestemming</td>
      <td class="tg-0lax">Shipment sorted at IMEC in destination country.</td>
      <td class="tg-0lax">31, Zending klaar voor transport naar land van bestemming</td>
    </tr>
    <tr>
      <td class="tg-0lax">A41</td>
      <td class="tg-0lax">Klantenservice Extra@Home heeft contact gehad</td>
      <td class="tg-0lax">Extra@Home Customer Service has made contact</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">A46</td>
      <td class="tg-0lax">Verzoek van ontvanger tot retour sturen door afhaallocatie</td>
      <td class="tg-0lax">Recipient request for pick-up location to return shipment</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">A73</td>
      <td class="tg-0lax">Zending is gecollecteerd door partner</td>
      <td class="tg-0lax">Shipment has been collected by partner</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">A94</td>
      <td class="tg-0lax">Zelf bezorging gewijzigd</td>
      <td class="tg-0lax">Delivery changed by customer</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">B06</td>
      <td class="tg-0lax">Zending geaccepteerd door PostNL</td>
      <td class="tg-0lax">Shipment accepted by PostNL IMEC.</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">C02</td>
      <td class="tg-0lax">Gescand bij PostNL-selfservicepunt</td>
      <td class="tg-0lax">Scanned at PostNL service point</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>        
    <tr>
      <td class="tg-0lax">H15</td>
      <td class="tg-0lax">Zending te groot of te zwaar, retour afzender</td>
      <td class="tg-0lax">Shipment too large or too heavy, return to sender</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">H17</td>
      <td class="tg-0lax">Waarde is hoger dan toegestaan door douane. Retour afzender.</td>
      <td class="tg-0lax">Value exceeds maximum customs value. Return to sender.</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">H18</td>
      <td class="tg-0lax">Bezorging niet gelukt, pakket gaat terug naar de afzender</td>
      <td class="tg-0lax">Delivery failed, package goes back to sender</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">H30</td>
      <td class="tg-0lax">Verzender heeft de zendingsopdracht geannuleerd</td>
      <td class="tg-0lax">Sender has cancelled the shipment order</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">J56</td>
      <td class="tg-0lax">We zijn onderweg om je zending af te halen</td>
      <td class="tg-0lax">We are en route to pickup address</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">J80</td>
      <td class="tg-0lax">Deze zending heeft nog geen afleverscan gekregen</td>
      <td class="tg-0lax">No delivery scan for this shipment yet</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">K25</td>
      <td class="tg-0lax">Zending vertraagd, locatie onbereikbaar voor verwerking</td>
      <td class="tg-0lax">Shipment delayed, location unreachable for processing</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">K71</td>
      <td class="tg-0lax">Bezorgen lukte niet, zending gaat naar PostNL-punt</td>
      <td class="tg-0lax">We missed you, shipment sent to PostNL retail point</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">P20</td>
      <td class="tg-0lax">Afgesproken plek is niet veilig, diefstalgevoelig</td>
      <td class="tg-0lax">Appointed place is not safe, prone to theft</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">P21</td>
      <td class="tg-0lax">Afgesproken plek is zichtbaar vanaf de straat, open gebied</td>
      <td class="tg-0lax">Appointed place is visible form the street, open area</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">P22</td>
      <td class="tg-0lax">Afgesproken plek is nat, niet overdekt</td>
      <td class="tg-0lax">Appointed place is wet, not covered</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">P23</td>
      <td class="tg-0lax">Afgesproken plek is niet toegankelijk/beschikbaar</td>
      <td class="tg-0lax">Appointed place is not accessible/available</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">P24</td>
      <td class="tg-0lax">Afgesproken plek volstaat niet, afmetingen pakket te groot</td>
      <td class="tg-0lax">Appointed place is not sufficient, package dimensions too large</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q14</td>
      <td class="tg-0lax">Zending uit transport gehaald voor controle</td>
      <td class="tg-0lax">Shipment removed from transport for inspection</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q16</td>
      <td class="tg-0lax">Pakket in depot, gaat onderweg naar land van bestemming</td>
      <td class="tg-0lax">Package in depot, goes enroute to country of destination</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q17</td>
      <td class="tg-0lax">Je pakket is klaar voor verzending naar Europa</td>
      <td class="tg-0lax">Your parcel is ready for shipment to Europe</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q18</td>
      <td class="tg-0lax">Je pakket is klaar voor verzending naar Nederland</td>
      <td class="tg-0lax">Your parcel is ready for shipment to The Netherlands</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Q19</td>
      <td class="tg-0lax">Je pakket is onderweg, het is nog niet ontvangen door PostNL</td>
      <td class="tg-0lax">Shipment still in transit</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">X16</td>
      <td class="tg-0lax">Zending voorgemeld en gesorteerd door PostNL</td>
      <td class="tg-0lax">Shipment pre-alerted by PostNL and sorted at IMEC.</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">X52</td>
      <td class="tg-0lax">Je zending wacht op bezorging in het land van bestemming</td>
      <td class="tg-0lax">Your parcel is awaiting delivery in the destination country</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y45</td>
      <td class="tg-0lax">Pakket definitief uit proces gehaald i.v.m. verboden inhoud.</td>
      <td class="tg-0lax">Parcel permanently removed from process due to prohibited contents.</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y46</td>
      <td class="tg-0lax">Pakket overschrijdt douanewaarde, transport is uitgesteld</td>
      <td class="tg-0lax">Parcel exceeds customs value, transport is postponed</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y47</td>
      <td class="tg-0lax">Retour afzender: ontbrekend/onjuist exportformulier</td>
      <td class="tg-0lax">Return to sender because of a missing/incorrect export form</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y48</td>
      <td class="tg-0lax">Pakket onbestelbaar: fout exportformulier & geen retouradres</td>
      <td class="tg-0lax">Parcel is undeliverable: incorrect export form and  missing return adress</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y64</td>
      <td class="tg-0lax">Vertraging  door&nbsp;&nbsp;&nbsp;importcontrole  in land van bestemming</td>
      <td class="tg-0lax">Sorry, delay due to import controls in destination country</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y65</td>
      <td class="tg-0lax">Je zending is vertraagd door extreme weersomstandigheden</td>
      <td class="tg-0lax">Sorry, shipment delayed due to extreme weather conditions</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
    <tr>
      <td class="tg-0lax">Y66</td>
      <td class="tg-0lax">Sorry, je zending is vertraagd door IT-problemen</td>
      <td class="tg-0lax">Sorry, your shipment has been delayed due to IT issues</td>
      <td class="tg-0lax">99, Niet van toepassing</td>
    </tr>
  </tbody>
</table>