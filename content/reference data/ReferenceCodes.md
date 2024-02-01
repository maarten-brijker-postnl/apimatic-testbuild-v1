# Reference Codes

# Printer types
    
GraphicFile|GIF 200 dpi<br>
GraphicFile|GIF 300 dpi<br>
GraphicFile|GIF 600 dpi

GraphicFile|JPG 200 dpi<br>
GraphicFile|JPG 300 dpi<br>
GraphicFile|JPG 600 dpi

GraphicFile|PDF

GraphicFile|PDF|MergeA 

Zebra|Generic ZPL II 200 dpi*<br>
Zebra|Generic ZPL II 300 dpi*<br>
Zebra|Generic ZPL II 600 dpi*

\* It is not recommended to send .pdf files/labels directly to a Zebra printer If you want to send it directly to your Zebra printer, please use .gif files or the native (generic) zpl printer type.

# Printing quality

When submitting a call to the Shipping or Labelling API be sure to check if the requested printer type matches the supported dpi specifications of your printer. The following documentation contains information on how to improve the quality of your printed shipping labels.

<a href="https://www.postnl.nl/Images/printkwaliteit-verzendlabels_tcm10-227254.pdf" target="_blank" rel="noopener noreferrer">Documentation Printing quality</a>

# Label types

The Label type helps you to determine what document will be returned. In most cases, only a Label is returned. The following label types are possible:

<table>
  <thead>
    <tr>
      <th>Labeltype</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Label (A6)</td>
      <td>normal shipping label for all shipments except for Parcels Non-EU</td>
    </tr>
    <tr>
      <td>BusPakjeExtra (A6)</td>
      <td>shipping label for parcels that fit in a mailbox</td>
    </tr>
    <tr>
      <td>CODcard (Kabinet (21 x 10,16 cm)</td>
      <td>COD card as required for Dutch domestic COD shipments</td>
    </tr>
    <tr>
      <td>CN23 form (A5)</td>
      <td>customs form for Parcels Non-EU shipments</td>
    </tr>
    <tr>
      <td>CP71 form (A5)</td>
      <td>customs form for Parcels Non-EU shipments</td>
    </tr>
    <tr>
      <td>Commercialinvoice (A4)</td>
      <td>commercial invoice for Parcels Non-EU shipments</td>
    </tr>
    <tr>
      <td>Return Label (A6)</td>
      <td>normal shipping label for reverse logistics</td>
    </tr>
  </tbody>
</table>

# Address types

PostNL internal applications validate the receiver address. In case the spelling of addresses should be different according to our PostNL information, the address details will be corrected. This can be noticed in Track & Trace.

The API will not add address details. Street and City fields will only be printed when they are in the call towards the Shipping or Labelling API.

The element Address type is a code in the request. Possible values are:

<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>01</td>
      <td>Receiver</td>
    </tr>
    <tr>
      <td>02</td>
      <td>Sender</td>
    </tr>
    <tr>
      <td>03</td>
      <td>Alternative sender address</td>
    </tr>
    <tr>
      <td>04</td>
      <td>Collection address</td>
    </tr>
    <tr>
      <td>08</td>
      <td>Return address*</td>
    </tr>
    <tr>
      <td>09</td>
      <td>Delivery address (for use with Pick up at PostNL location)</td>
    </tr>
  </tbody>
</table>

\* When using the ‘label in the box return label’, it is mandatory to use an Antwoordnummer in AddressType 08. This cannot be a regular address. 

# Contact types

Contact type has the elements Email, SMSNr and TelNr. These fields have a dependency with each other. At least one of these three fields must be filled mandatory for certain products/ product codes (e.g. Evening/Sameday delivery, Pickup at PostNL location). Two or three can be filled as well.

<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>01</td>
      <td>Receiver</td>
    </tr>
    <tr>
      <td>02</td>
      <td>Sender</td>
    </tr>
  </tbody>
</table>

Remark: Please add the e-mail address of the receiver to improve the Mijn PostNL experience of your customer.

# Amount types

<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>01</td>
      <td>Cash on Delivery (COD)</td>
    </tr>
    <tr>
      <td>02</td>
      <td>Insurance amount</td>
    </tr>
  </tbody>
</table>

# Group types

<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>01</td>
      <td>Collection request</td>
    </tr>
    <tr>
      <td>03</td>
      <td>Multiple parcels in one shipment (multicollo) </td>
    </tr>
    <tr>
      <td>04</td>
      <td>Single parcel in one shipment</td>
    </tr>
  </tbody>
</table>

# Transaction codes

<table>
  <thead>
    <tr>
      <th>Transaction Code</th>
      <th>Transaction Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>11</td>
      <td>Sale of goods</td>
    </tr>
    <tr>
      <td>21</td>
      <td>Returned goods</td>
    </tr>
    <tr>
      <td>31</td>
      <td>Gift</td>
    </tr>
    <tr>
      <td>32</td>
      <td>Commercial sample</td>
    </tr>
    <tr>
      <td>91</td>
      <td>Documents</td>
    </tr>
  </tbody>
  </table>

# Delivery options

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Daytime</td>
      <td>Daytime delivery</td>
    </tr>
    <tr>
      <td>Evening</td>
      <td>Evening delivery</td>
    </tr>
    <tr>
      <td>Sunday</td>
      <td>Sunday delivery</td>
    </tr>
    <tr>
      <td>Today*</td>
      <td>Delivery on day of handover to PostNL</td>
    </tr>
    <tr>
      <td>Sameday</td>
      <td>Sameday delivery</td>
    </tr>
    <tr>
      <td>Morning Delivery<br>08:00-10:00</td>
      <td>Guaranteed delivery between the timeframe specified</td>
    </tr>
    <tr>
      <td>Noon Delivery<br>08:00-12:00</td>
      <td>Guaranteed delivery between the timeframe specified</td>
    </tr>
    <tr>
      <td>Afternoon Delivery<br>08:00-17:00</td>
      <td>Guaranteed delivery between the timeframe specified</td>
    </tr>
    <tr>
      <td>Pickup</td>
      <td>Pickup at PostNL location</td>
    </tr>
  </tbody>
</table>


\* The Today delivery option will be returned on any given day (Mon – Sun) but will only be possible on the first following business day.

**Checkout API**

All the above delivery options can be used in the request of the Checkout API. 

**Deliverydate and Timeframe API**

The names of the guaranteed options differ.

<table>
  <thead>
    <tr>
      <th>Option</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Morning</td>
      <td>Guaranteed delivery between the timeframe 08:00-10:00</td>
    </tr>
    <tr>
      <td>Noon</td>
      <td>Guaranteed delivery between the timeframe 08:00-12:00</td>
    </tr>
    <tr>
      <td>Afternoon</td>
      <td>Guaranteed delivery between the timeframe 08:00-17:00</td>
    </tr>
  </tbody>
</table>

The ‘Pickup’ option is not available in the Deliverydate and Timeframe API. If you want to retrieve pickup locations, you can use the Checkout or Location API. 

PostNL will charge an additional amount for delivery of the parcels with the options Evening, Morning, (After)Noon, Sameday, Delivery on demand, Guaranteed delivery, Sunday and Today. For specific costs and the activation of this delivery options, it is recommended to consult your PostNL Parcels account manager. For Sunday, Sameday and Today delivery it is even mandatory to consult your account manager. 

# Sustainability codes

You can show customers when their parcel can be delivered sustainably. In the response of the API the follow sustainability codes be distinguished:

<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>00</td>
      <td>Sustainability score not available</td>
    </tr>
    <tr>
      <td>01</td>
      <td>Sustainable delivery</td>
    </tr>
    <tr>
      <td>02</td>
      <td>Sustainable option</td>
    </tr>
    <tr>
      <td>03</td>
      <td>Sustainable delivery + sustainable option</td>
    </tr>
  </tbody>
</table>

You can build in the corresponding communication messages in your checkout; 

Sustainably delivery;  “Duurzaam bezorgd”

Sustainable option;  “Duurzame optie”

Not available: Not a sustainable option (yet).

Please refer to the <a href="https://developer.postnl.nl/browse-apis/checkout/checkout-api/" target="_blank" rel="noopener noreferrer">Guidelines</a> for more information about Sustainability