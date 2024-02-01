# Error Codes

# Generic
    
<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>The username/password  combination is incorrect.</td>
    </tr>
    <tr>
      <td>10</td>
      <td>Service is currently  disabled</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>Check Exception in the  detail section</td>
    </tr>
    <tr>
      <td>1001</td>
      <td>API Framework Message  Interceptor</td>
    </tr>
    <tr>
      <td>1002</td>
      <td>Exception occured,  Message: {0}, stacktrace {1}.</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Exception occured  connecting to a backend service.</td>
    </tr>
    <tr>
      <td>13</td>
      <td>Exception occured: {0}</td>
    </tr>
    <tr>
      <td>16</td>
      <td>{0} not found.</td>
    </tr>
    <tr>
      <td>17</td>
      <td>Message validation  failed due to incorrect message format</td>
    </tr>
    <tr>
      <td>2</td>
      <td>The user is not  authorized for the method '{0}'.</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Username/password is  not specified.</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Required parameter  '{0}' is missing.</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Value '{0}' is not in  the correct format '{1}'.</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Value '{0}' is not in  the correct range '{1} - {2}'.</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Parameter '{0}' may  not be null</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Parameter '{0}' must  be null.</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Number of requests  exceed the maximum of {0} requests/second</td>
    </tr>
  </tbody>
</table>

# Send & Track Errors

<table>
    <thead>
        <tr>
            <th>Error code</th>
            <th>Error message</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>11(ContactType)02</td>
            <td>Email of (ContactType) is required</td>
        </tr>
        <tr>
            <td>11(ContactType)03</td>
            <td>Phone number of (ContactType) is required</td>
        </tr>
        <tr>
            <td>11(ContactType)04</td>
            <td>Email or phone number of (ContactType) is required</td>
        </tr>
        <tr>
            <td>11(ContactType)06</td>
            <td>Email does not meet the correct format</td>
        </tr>
        <tr>
            <td>127{AddressType}02</td>
            <td>AddressType {AddressType} is required</td>
        </tr>
        <tr>
            <td>127{AddressType}03</td>
            <td>Country of AddressType {AddressType} is required</td>
        </tr>
        <tr>
            <td>127{AddressType}04</td>
            <td>Country parameter is required</td>
        </tr>
        <tr>
            <td>127{AddressType}05</td>
            <td>Only {CountryCode} is allowed for AddressType {AddressType}</td>
        </tr>
        <tr>
            <td>127{AddressType}06</td>
            <td>{CountryCode} is not allowed for AddressType {AddressType}</td>
        </tr>
        <tr>
            <td>127{AddressType}07</td>
            <td>The country in AddressType {AddressType} must be a country in {TextGroup}</td>
        </tr>
        <tr>
            <td>127{AddressType}08</td>
            <td>The country in AddressType {AddressType} must be outside {TextGroup}</td>
        </tr>
        <tr>
            <td>128{AddressType}01</td>
            <td>Country of AddressType {AddressType} is required</td>
        </tr>
        <tr>
            <td>128{AddressType}02</td>
            <td>Incorrect address specified in AddressType {AddressType}</td>
        </tr>
        <tr>
            <td>128{AddressType}03</td>
            <td>Address is unknown</td>
        </tr>
        <tr>
            <td>10400{AddressType}</td>
            <td>An Antwoordnummer is not allowed for AddressType XX</td>
        </tr>
        <tr>
            <td>10401{AddressType}</td>
            <td>Address is missing for AddressType XX</td>
        </tr>
        <tr>
            <td>10404(AddressType)</td>
            <td>Address is missing for AddressType (AddressType)</td>
        </tr>
        <tr>
            <td>10405(AddressType)</td>
            <td>AddressType (AddressType) must be an Antwoordnummer</td>
        </tr>
        <tr>
            <td>10601</td>
            <td>Receiver address cannot be a postal box</td>
        </tr>
        <tr>
            <td>10602</td>
            <td>Receiver address is required</td>
        </tr>
        <tr>
            <td>10701</td>
            <td>Barcode is not a valid S10-barcode</td>
        </tr>
        <tr>
            <td>10701</td>
            <td>Barcode is not a valid S10-barcode</td>
        </tr>
        <tr>
            <td>10702</td>
            <td>Barcode is required</td>
        </tr>
        <tr>
            <td>10801</td>
            <td>Receiver address cannot be from 'Waddeneilanden'</td>
        </tr>
        <tr>
            <td>10802</td>
            <td>Receiver zipcode is missing</td>
        </tr>
        <tr>
            <td>11000</td>
            <td>Missing configuration parameter Contacttype</td>
        </tr>
        <tr>
            <td>11001</td>
            <td>No data in the Collo found matching the configured ContactType or a non-existend ContactType configured</td>
        </tr>
        <tr>
            <td>11008</td>
            <td>Taal only accepts characters A-Z with a length of 2.</td>
        </tr>
        <tr>
            <td>11101</td>
            <td>A 3S barcode and a 2S barcode is required</td>
        </tr>
        <tr>
            <td>11102</td>
            <td>The barcode is not a valid 3S</td>
        </tr>
        <tr>
            <td>11103</td>
            <td>The barcode is not a valid 2S</td>
        </tr>
        <tr>
            <td>11104</td>
            <td>Parcel count and parcel number cannot differ from 1</td>
        </tr>
        <tr>
            <td>11501</td>
            <td>Empty request data</td>
        </tr>
        <tr>
            <td>11502</td>
            <td>Receiver city is required</td>
        </tr>
        <tr>
            <td>11503</td>
            <td>Receiver street is required</td>
        </tr>
        <tr>
            <td>11504</td>
            <td>Parcel weight is required</td>
        </tr>
        <tr>
            <td>11505</td>
            <td>For this product the ExternalCharacteristic is required.</td>
        </tr>
        <tr>
            <td>11601</td>
            <td>Commercial Product must contain CommProduct with fields: Code max 5 digits, Type max 3 digits.</td>
        </tr>
        <tr>
            <td>11602</td>
            <td>Commercial Product must contain Product with fields: Code max 5 digits. Optionally it may contain: Cat max length of 2, Line max length of 3, Type max length of 6, Soort max length of 4.</td>
        </tr>
        <tr>
            <td>11603</td>
            <td>Commercial Services must contain the following fields: Service Group Code max length of 3, Charge Code max length of 2, Characteristic Code max 3 digits, Value Code max 3 digits. Optionally it may contain: Value AddInfoType max length of 8 and Value AddInfoWaarde max length of 35</td>
        </tr>
        <tr>
            <td>11604</td>
            <td>If Commercial product contains a Bundel it has to have fields: Code max length of 10, Type max length of 1.</td>
        </tr>
        <tr>
            <td>12209</td>
            <td>Delivery/Pickup} date is required</td>
        </tr>
        <tr>
            <td>12210</td>
            <td>{Delivery/Pickup} date is in incorrect format</td>
        </tr>
        <tr>
            <td>12213</td>
            <td>Receiver House Number is missing</td>
        </tr>
        <tr>
            <td>12214</td>
            <td>Receiver Post Code is missing</td>
        </tr>
        <tr>
            <td>12215</td>
            <td>Receiver Country is missing</td>
        </tr>
        <tr>
            <td>12216</td>
            <td>Unable to call the back-end webservice</td>
        </tr>
        <tr>
            <td>12701</td>
            <td>AddressType parameter is required</td>
        </tr>
        <tr>
            <td>12804</td>
            <td>AddressType is required</td>
        </tr>
        <tr>
            <td>13301</td>
            <td>Evening Delivery not possible for this product code</td>
        </tr>
        <tr>
            <td>13303</td>
            <td>The product code for Check at the door is incorrect</td>
        </tr>
        <tr>
            <td>13304</td>
            <td>Sunday Delivery is not available for this product code</td>
        </tr>
        <tr>
            <td>13701</td>
            <td>COD is not allowed for this product</td>
        </tr>
        <tr>
            <td>13702</td>
            <td>The parent shipment requires a COD amount</td>
        </tr>
        <tr>
            <td>13703</td>
            <td>The parent shipment requires an IBAN number</td>
        </tr>
        <tr>
            <td>13704</td>
            <td>The child shipment cannot contain a COD value</td>
        </tr>
        <tr>
            <td>13705</td>
            <td>The child shipment cannot contain an IBAN number</td>
        </tr>
        <tr>
            <td>13706</td>
            <td>The COD value is invalid</td>
        </tr>
        <tr>
            <td>13707</td>
            <td>The COD value is too large for this product; it cannot exceed {MaxAmount} EUR</td>
        </tr>
        <tr>
            <td>13708</td>
            <td>Length of BIC must be between 8 and 11.</td>
        </tr>
        <tr>
            <td>13801</td>
            <td>Insurance is not allowed for this product</td>
        </tr>
        <tr>
            <td>13903</td>
            <td>Client number is not filled out</td>
        </tr>
        <tr>
            <td>13904</td>
            <td>Client number must be a numeric value</td>
        </tr>
        <tr>
            <td>13905</td>
            <td>Article description is required</td>
        </tr>
        <tr>
            <td>13907</td>
            <td>Country is required</td>
        </tr>
        <tr>
            <td>13909</td>
            <td>Volume is required</td>
        </tr>
        <tr>
            <td>13910</td>
            <td>Volume {Volume} must be no longer than 9 digits and contain only numeric characters</td>
        </tr>
        <tr>
            <td>13911</td>
            <td>Parcel weight is required</td>
        </tr>
        <tr>
            <td>13912</td>
            <td>Weight {Weight} should contain only numeric characters and can't be greater than 99999</td>
        </tr>
        <tr>
            <td>13913</td>
            <td>Receiver Mobile is required</td>
        </tr>
        <tr>
            <td>13914</td>
            <td>Receiver Mobile {Mobile} must be within 16 characters</td>
        </tr>
        <tr>
            <td>13915</td>
            <td>Receiver email is required</td>
        </tr>
        <tr>
            <td>13916</td>
            <td>Receiver email {Email} must be within 50 alphanumeric characters and should be in correct format</td>
        </tr>
        <tr>
            <td>13917</td>
            <td>ExternalCharacteristic is required</td>
        </tr>
        <tr>
            <td>13918</td>
            <td>ExternalCharacteristic has a maximum length of 35</td>
        </tr>
        <tr>
            <td>14001</td>
            <td>Barcode is required</td>
        </tr>
        <tr>
            <td>14002</td>
            <td>Barcode length must be 13 characters</td>
        </tr>
        <tr>
            <td>14003</td>
            <td>Barcode is not a valid 3S barcode</td>
        </tr>
        <tr>
            <td>14101</td>
            <td>DNP Barcode is required</td>
        </tr>
        <tr>
            <td>14102</td>
            <td>DNP Contract ID is required</td>
        </tr>
        <tr>
            <td>15001</td>
            <td>Downstream barcode is not defined</td>
        </tr>
        <tr>
            <td>15002</td>
            <td>DNP barcode is not a valid S10 barcode</td>
        </tr>
        <tr>
            <td>15201</td>
            <td>Country code GG should be used for addresses in Guernsey</td>
        </tr>
        <tr>
            <td>15202</td>
            <td>Country code JE should be used for addresses in Jersey</td>
        </tr>
        <tr>
            <td>15203</td>
            <td>Country code IM should be used for addresses in Isle of Man</td>
        </tr>
        <tr>
            <td>15204</td>
            <td>Country code IC should be used for addresses in Las Palmas</td>
        </tr>
        <tr>
            <td>15205</td>
            <td>Country code IC should be used for addresses in Santa Cruz</td>
        </tr>
        <tr>
            <td>15206</td>
            <td>Country code EA should be used for addresses in Melilla</td>
        </tr>
        <tr>
            <td>15403</td>
            <td>Date of birth is required</td>
        </tr>
        <tr>
            <td>15501</td>
            <td>Location ID is required</td>
        </tr>
        <tr>
            <td>15502</td>
            <td>Contract ID is required</td>
        </tr>
        <tr>
            <td>15503</td>
            <td>Receiver ID (door code) is required</td>
        </tr>
        <tr>
            <td>15701</td>
            <td>Contract ID not allowed in combination with this product</td>
        </tr>
        <tr>
            <td>16201</td>
            <td>Barcode is required</td>
        </tr>
        <tr>
            <td>16202</td>
            <td>Length of 2S type barcode must be between 11 and 15</td>
        </tr>
        <tr>
            <td>16203</td>
            <td>Barcode is not a valid 2S barcode</td>
        </tr>
        <tr>
            <td>16301</td>
            <td>Customs segment is required</td>
        </tr>
        <tr>
            <td>16301</td>
            <td>Barcode is required</td>
        </tr>
        <tr>
            <td>16302</td>
            <td>GlobalPack customs are required</td>
        </tr>
        <tr>
            <td>16302</td>
            <td>Length of 3S type barcode must be between 12 and 15</td>
        </tr>
        <tr>
            <td>16303</td>
            <td>Parcel weight is not an integer</td>
        </tr>
        <tr>
            <td>16303</td>
            <td>Barcode is not a valid 3S barcode</td>
        </tr>
        <tr>
            <td>16304</td>
            <td>Weight cannot exceed 20000 grams</td>
        </tr>
        <tr>
            <td>16304</td>
            <td>Weight cannot exceed 30000 grams</td>
        </tr>
        <tr>
            <td>16305</td>
            <td>DouaneVerklaring.VerklaringsRegel is required</td>
        </tr>
        <tr>
            <td>16306</td>
            <td>Parcel weight is required</td>
        </tr>
        <tr>
            <td>16308</td>
            <td>Field HSTariffNr must be between 8 and 10</td>
        </tr>
        <tr>
            <td>16309</td>
            <td>Field Description must be between 1 and 200 long and is required.</td>
        </tr>
        <tr>
            <td>16310</td>
            <td>Field Quantity must be between 1 and 10 long and is required.</td>
        </tr>
        <tr>
            <td>16311</td>
            <td>Field Weigth must be between 1 and 10 long and is required.</td>
        </tr>
        <tr>
            <td>16312</td>
            <td>Field Value must be between 1 and 8 long and is required.</td>
        </tr>
        <tr>
            <td>16313</td>
            <td>Field ValutaCd must be between 1 and 3 long and is required.</td>
        </tr>
        <tr>
            <td>16314</td>
            <td>Field CountryOfOrigin must be between 1 and 2.</td>
        </tr>
        <tr>
            <td>19001</td>
            <td>AddressType parameter is required</td>
        </tr>
        <tr>
            <td>19002{AddressType}</td>
            <td>AddressType {group 1} and {group 2} is required</td>
        </tr>
        <tr>
            <td>19003{AddressType}</td>
            <td>Country with AddressType {group 1} and {group 2} is required</td>
        </tr>
        <tr>
            <td>19004{AddressType}</td>
            <td>Country parameter is required</td>
        </tr>
        <tr>
            <td>19005{AddressType}</td>
            <td>Countries in {group 1} and {group 2} address not allowed together for this product</td>
        </tr>
        <tr>
            <td>20001</td>
            <td>Verwachtingssegment is required</td>
        </tr>
        <tr>
            <td>20002</td>
            <td>End DateTime is required</td>
        </tr>
        <tr>
            <td>20003</td>
            <td>VerwachtingSrt Code is required</td>
        </tr>
        <tr>
            <td>20004</td>
            <td>VerwachtingSrt Code is not a valid {OnDemand} VerwachtingSrt Code</td>
        </tr>
        <tr>
            <td>20005</td>
            <td>Start DateTime is after End DateTime</td>
        </tr>
        <tr>
            <td>20006</td>
            <td>DateTime range not within same calendar day</td>
        </tr>
        <tr>
            <td>20007</td>
            <td>Chosen date not possible</td>
        </tr>
        <tr>
            <td>20008</td>
            <td>A date more than seven days in the future is not allowed</td>
        </tr>
        <tr>
            <td>20009</td>
            <td>Start DateTime is required</td>
        </tr>
        <tr>
            <td>20401</td>
            <td>GevaarlStofCd is required</td>
        </tr>
        <tr>
            <td>20403</td>
            <td>ADRPuntenAantis required</td>
        </tr>
        <tr>
            <td>20404</td>
            <td>TunnelCdis required</td>
        </tr>
        <tr>
            <td>20406</td>
            <td>VerpakkingsGrpOmschris required</td>
        </tr>
        <tr>
            <td>20407</td>
            <td>BrutoGewichtis required</td>
        </tr>
        <tr>
            <td>20408</td>
            <td>UNDGNris required</td>
        </tr>
        <tr>
            <td>20409</td>
            <td>TransportCategorieCdis required</td>
        </tr>
        <tr>
            <td>20410</td>
            <td>ChemTechOmschris required</td>
        </tr>
        <tr>
            <td>20411</td>
            <td>TunnelCd has a maximum length of 6</td>
        </tr>
        <tr>
            <td>20412</td>
            <td>VerpakkingsGrpCd has a maximum length of 3</td>
        </tr>
        <tr>
            <td>20413</td>
            <td>VerpakkingsGrpOmschr has a maximum length of 30</td>
        </tr>
        <tr>
            <td>20414</td>
            <td>ChemTechOmschr has a maximum length of 30</td>
        </tr>
        <tr>
            <td>20415</td>
            <td>GevaarlStofCd must be an integer and has a maximum length of 3 positions</td>
        </tr>
        <tr>
            <td>20416</td>
            <td>ADRPuntenAant must be an integer and has a maximum length of 5 positions</td>
        </tr>
        <tr>
            <td>20417</td>
            <td>BrutoGewicht must be an integer and has a maximum length of 7 positions</td>
        </tr>
        <tr>
            <td>20418</td>
            <td>UNDGNr must be an integer and has a maximum length of 4 positions</td>
        </tr>
        <tr>
            <td>20419</td>
            <td>TransportCategorieCd must be an integer and has a maximum length of 1 positions</td>
        </tr>
        <tr>
            <td>20420</td>
            <td>GevaarlStof is required</td>
        </tr>
        <tr>
            <td>20501</td>
            <td>Barcode is required</td>
        </tr>
        <tr>
            <td>20502</td>
            <td>Barcode (barcode) is not a valid barcode</td>
        </tr>
        <tr>
            <td>21001</td>
            <td>Total number of colli in the shipment doesn't match with the amount of barcodes.</td>
        </tr>
        <tr>
            <td>21002</td>
            <td>Total number of colli is invalid. </td>
        </tr>
        <tr>
            <td>21003</td>
            <td>Count of colli is invalid. </td>
        </tr>
        <tr>
            <td>21004</td>
            <td>The count is too large for Main Barcode {Main Barcode}</td>
        </tr>
        <tr>
            <td>21005</td>
            <td>Barcodes of Main Barcode  {Main Barcode} must be unique.</td>
        </tr>
        <tr>
            <td>21006</td>
            <td>Main Barcode  {Main Barcode} contains invalid shipment(s)</td>
        </tr>
        <tr>
            <td>21201</td>
            <td>Customer number, small business number or consumer number is required</td>
        </tr>
        <tr>
            <td>21202</td>
            <td>Customer code is required</td>
        </tr>
        <tr>
            <td>21203</td>
            <td>UPN must be an integer and has a maximum length of 8 positions.</td>
        </tr>
        <tr>
            <td>21204</td>
            <td>Customer number must be an integer and has a maximum length of 10 positions.</td>
        </tr>
        <tr>
            <td>21205</td>
            <td>Field Customer code exceeds the maximum of 6 characters</td>
        </tr>
        <tr>
            <td>21401</td>
            <td>BLS code, {procAannVerw / procAann}, must be an integer and must have a length of 6 positions.</td>
        </tr>
        <tr>
            <td>21501</td>
            <td>Barcode is required</td>
        </tr>
        <tr>
            <td>21502</td>
            <td>Barcode is not a valid UPS barcode.</td>
        </tr>
        <tr>
            <td>22001</td>
            <td>Field Omschrijving must be between 1 and 200 long and is required.</td>
        </tr>
        <tr>
            <td>22001</td>
            <td>Field Aantal must be between 1 and 10 long and is required.</td>
        </tr>
        <tr>
            <td>22001</td>
            <td>Field Gewicht must be between 1 and 10 long and is required.</td>
        </tr>
        <tr>
            <td>22001</td>
            <td>Field Geldsom must be between 1 and 8 long and is required.</td>
        </tr>
        <tr>
            <td>22001</td>
            <td>Field ValutaCd must be between 1 and 3 long and is required.</td>
        </tr>
        <tr>
            <td>22002</td>
            <td>Field LandVanHerkomst must be between 1 and 2.</td>
        </tr>
        <tr>
            <td>24001</td>
            <td>Shipment was rejected by SVS</td>
        </tr>
        <tr>
            <td>30002</td>
            <td>Order cannot be canceled because no valid product code found in EP. Reason code: NO_PICKUP_ORDER_IN_PRODUCT_CODE</td>
        </tr>
        <tr>
            <td>1225000</td>
            <td>Request format is invalid</td>
        </tr>
        <tr>
            <td>1225002</td>
            <td>SystemId required in the request</td>
        </tr>
        <tr>
            <td>1225003</td>
            <td>ExpectedDeliveryDate required in the request</td>
        </tr>
        <tr>
            <td>1225004</td>
            <td>Timeframes expected in combination with requested Product</td>
        </tr>
        <tr>
            <td>1225005</td>
            <td>CommercialProduct required in the request</td>
        </tr>
        <tr>
            <td>1225006</td>
            <td>ServiceGroup required in the request</td>
        </tr>
        <tr>
            <td>1225007</td>
            <td>Characteristic required in the request</td>
        </tr>
        <tr>
            <td>1225008</td>
            <td>Value required in the request</td>
        </tr>
        <tr>
            <td>1225009</td>
            <td>The provided combination of values for ProductService is invalid</td>
        </tr>
        <tr>
            <td>1225010</td>
            <td>AddressCat 01 required in the request</td>
        </tr>
        <tr>
            <td>1225011</td>
            <td>Invalid AddressType</td>
        </tr>
        <tr>
            <td>1225012</td>
            <td>CountryCode required in the request</td>
        </tr>
        <tr>
            <td>1225013</td>
            <td>Invalid country code</td>
        </tr>
        <tr>
            <td>1225014</td>
            <td>PostalCode required in the request</td>
        </tr>
        <tr>
            <td>1225015</td>
            <td>The provided Postal code format is invalid</td>
        </tr>
        <tr>
            <td>1225016</td>
            <td>Postal code could not be found</td>
        </tr>
        <tr>
            <td>1225017</td>
            <td>Invalid day of the week</td>
        </tr>
        <tr>
            <td>1225029</td>
            <td>Service is not available for the requested postal code on specific weekday</td>
        </tr>
        <tr>
            <td>1225030</td>
            <td>Service is not possible due to holidays </td>
        </tr>
        <tr>
            <td>1225031</td>
            <td>Service is not possible due to deviating distribution schedules</td>
        </tr>
        <tr>
            <td>1225032 </td>
            <td>Unknown error for ValidateDeliveryDate</td>
        </tr>
    </tbody>
</table>

# Send & Track Warnings

<table>
    <thead>
        <th>Warning code</th>
        <th>Description</th>
    </thead>
    <tbody>
        <tr>
            <td>11(ContactType)07</td>
            <td>Email is longer than 50 characters</td>
        </tr>
        <tr>
            <td>128{AddressType}03</td>
            <td>Address is unknown</td>
        </tr>
        <tr>
            <td>10402</td>
            <td>Unable to call the back-end webservice</td>
        </tr>
        <tr>
            <td>16307</td>
            <td>Field HSTariffNr must be between 6 and 10</td>
        </tr>
        <tr>
            <td>17809</td>
            <td>COD value for shipment {barCode} has been removed, product is not a COD product.</td>
        </tr>
        <tr>
            <td>17810</td>
            <td>Insured value for shipment {barCode} has been removed, product is not an insured product.</td>
        </tr>
        <tr>
            <td>17811</td>
            <td>Contact type was changed to 01 (receiver) because we didn't receive a contact type</td>
        </tr>
        <tr>
            <td>17812</td>
            <td>Contact information was removed because there is no valid contact type</td>
        </tr>
        <tr>
            <td>176{AddressType}01</td>
            <td>Postcode is invalid or missing in address type {AddressType}.</td>
        </tr>
        <tr>
            <td>176{AddressType}02</td>
            <td>Home number is missing in address type {AddressType}.</td>
        </tr>
        <tr>
            <td>176{AddressType}03</td>
            <td>The combination of Postcode and Home number has not been found for address type {AddressType}</td>
        </tr>
    </tbody>
</table>

# Checkout & Delivery Options

**Location API**

<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>Message</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>10</td>
      <td>No results found</td>
    </tr>
    <tr>
      <td>3000</td>
      <td>Request format is invalid</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>{0} required in the request</td>
    </tr>
    <tr>
      <td>3002</td>
      <td>The provided {0} format is&nbsp;&nbsp;&nbsp;invalid</td>
    </tr>
    <tr>
      <td>3003</td>
      <td>Expected {0} for {1} but was {2}</td>
    </tr>
  </tbody>
</table>

**Deliverydate API**

<table>
  <thead>
    <tr>
      <th>Error code</th>
      <th>Message based on presence field</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3001</td>
      <td>OrderDateTime required in the request</td>
    </tr>
    <tr>
      <td>3000</td>
      <td>Error: Request format is invalid</td>
    </tr>
    <tr>
      <td>3003</td>
      <td>Expected {X or Y} for {Field} but was {Z}</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>Postal code required in the request</td>
    </tr>
    <tr>
      <td>3010</td>
      <td>Postal code could not be found</td>
    </tr>
    <tr>
      <td>3002</td>
      <td>Postal code format is invalid (NL: postal code 6, BE postal code 4)</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>Countrycode required in the request</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>AddressCat 01 required in the request</td>
    </tr>
    <tr>
      <td>3004</td>
      <td>Provided combination of values of CommProductService is invalid</td>
    </tr>
  </tbody>
</table>

**Timeframe API**

<table>
  <thead>
    <tr>
      <th>Error code</th>
      <th>Message based on presence field</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3000</td>
      <td>Request format is invalid</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>From timeframe period required in the request</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>From timeframe period required in the request</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>Streetname requirend in the&nbsp;&nbsp;&nbsp;request</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>Postal code required in the&nbsp;&nbsp;&nbsp;request</td>
    </tr>
  </tbody>
</table>

**Checkout API**

<table>
  <thead>
    <tr>
      <th>Error code</th>
      <th>Message based on field content</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3000</td>
      <td>Error: Request format is invalid</td>
    </tr>
    <tr>
      <td>3006</td>
      <td>Expected TimeFramePeriode.To to be after TimeFramePeriod.From</td>
    </tr>
    <tr>
      <td>3002</td>
      <td>Only for AddressCat 01</td>
    </tr>
    <tr>
      <td>3010</td>
      <td>Postal code format is invalid. NL: postal code 6, BE postal&nbsp;&nbsp;&nbsp;code 4 (1000-9999) </td>
    </tr>
    <tr>
      <td>3003</td>
      <td>Only for AddressCat 01</td>
    </tr>
    <tr>
      <td>3001</td>
      <td>If an AddressCat is given but is not 01, then Address Cat 01 required</td>
    </tr>
    <tr>
      <td>3003</td>
      <td>If two AddressCat are given, (01 and the other is invalid) then Expected&nbsp;&nbsp;&nbsp;{01 or 02} for {AdressCat} but was {2}</td>
    </tr>
    <tr>
      <td>3004</td>
      <td>Provided combination of values for ProductServices and country code is&nbsp;&nbsp;&nbsp;invalid</td>
    </tr>
    <tr>
      <td>3003</td>
      <td>Expected {0-7} for {DayOfTheWeek} but was {2}</td>
    </tr>
  </tbody>
</table>