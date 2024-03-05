# Shipping API Guidelines

### All-in-one Shipping API

This API combines the functionality of the existing Barcode, Labelling, Confirmation and Easy Return APIs. Integration of the Barcode API lets you generate unique barcodes for each shipment whilst cutting down on the number of API requests.

<details>
  <summary><b>All-in-one</b></summary>

**Shipping labels**

The label that are send to you is not suited for scaling, for the measures of the label are carefully designed to ease the parcel through our process.

**Barcodes**

It is possible to send a barcode in the request. But if you leave the barcode out of your request an unique barcode will be generated automatically. Please check the [Barcode API](https://docs.api.postnl.nl/#/http/api-endpoints/send-track/barcode/overview) page for specific barcode guidelines. 

*NOTE: This is not possible for additional barcodes in Label in the box (return barcode), multi-collo and Combilabels 'Parcels non EU' with productcode 4945 (downpartner barcode) shipment requests. And also International Mail & Packet products (PEPS) barcodes cannot be generated automatically by using this service.*

**Confirmation**

This API contains the possibility to create a label and the PostNL confirmation. This service sends the confirmation to the PostNL systems and upon receiving the confirmation, the service sends back a filled in label to print and to stick on the parcel.

With the Confirm boolean in the request (true of false), you can determine if you want to confirm the shipment in the same call or not.
</details>
<br>
