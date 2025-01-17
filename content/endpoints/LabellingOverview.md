# Labelling API

### Summary
    
* Reason to Call: Create a label and send a confirmation to PostNL (optional).
* Input: Information about the shipment.
* Output: One or more shipping labels.

Please note that you can use the all-in-one [Shipping API](#tag/Shipping) as well. This API combines the functionality of the Barcode, Labelling, Confirmation and Easy Return API. With this API you generate unique barcodes at the same time you create a label and so cutting down the number of API requests.

When using the [Shipping](#tag/Shipment) or Labelling API (With the Confirm boolean true in the request) the Confirming service does no longer need to be integrated in your system.

### Guidelines

At the <a href="https://developer.postnl.nl/" target="_blank" rel="noopener noreferrer">Developer Portal</a> you can find information about the use and functionality of the API. It is strongly recommended that you read this carefully before starting the implementation.

<button type="button">
  <a href="https://developer.postnl.nl/browse-apis/send-and-track/labelling-webservice/" target="_blank" rel="noopener noreferrer">Documentation</a>
</button>

### Versioning

#### REST:

<table>
  <tbody>
    <tr>
      <td>
        <strong>Version</strong>
      </td>
      <td>
        <strong>Release Date</strong>
      </td>
      <td>
        <strong>Status</strong>
      </td>
      <td>
        <strong>Release Notes</strong>
      </td>
      <td>
        <strong>Schema Changes</strong>
      </td>
    </tr>
    <tr>
      <td>2_1</td>
      <td>Jun 01, 2017</td>
      <td>Supported</td>
      <td>See below</td>
      <td>N/A</td>
    </tr>
    <tr>
      <td>2_2</td>
      <td>Jan 25, 2019</td>
      <td>Current version</td>
      <td>See below</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>

#### v2.2

**IN COMPARISON TO THE 2_0 SOAP VERSION**<br>
the following fields have been added to the interface, in order to implement a commercial route to China:<br>
* Shipment.Customs.Content.Content.EAN
* Shipment Customs.Content.Content.ProductURL

The following fields have been added to the interface for Delivery on Demand (Mytime):<br>
* DeliveryTimestampStart
* DeliveryTimestampEnd<br>
__NOTE: THIS PRODUCT NO LONGER EXIST__

#### v2.1

The following fields have been added to the interface for shipments to the USA:<br>    
* Shipment.Customs.TrustedShipperID
* Shipment.Customs.ImporterReferenceCode
* Shipment.Customs.TransactionCode
* Shipment.Customs.TransactionDescription
<br><br>
* Shipment.CodingText (response)<br>
A Codingtext have been added to the labels for mailbox parcels (brievenbuspakjes).

#### SOAP:

<table>
  <tbody>
    <tr>
      <td>
        <strong>Version</strong>
      </td>
      <td>
        <strong>Release Date</strong>
      </td>
      <td>
        <strong>Status</strong>
      </td>
      <td>
        <strong>Release Notes</strong>
      </td>
      <td>
        <strong>Schema Changes</strong>
      </td>
    </tr>
    <tr>
      <td>1_3</td>
      <td>Dec 27, 2012</td>
      <td>Not supported</td>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_4</td>
      <td>Nov 8, 2013</td>
      <td>Not supported</td>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_5</td>
      <td>Feb 27, 2014</td>
      <td>Not supported</td>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_6</td>
      <td>Aug 14, 2014</td>
      <td>Not supported</td>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_7</td>
      <td>Nov 14, 2014</td>
      <td>Not supported</td>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_8</td>
      <td>Jan 12, 2015</td>
      <td>Not supported</td>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_9</td>
      <td>Apr 24, 2015</td>
      <td>Not supported</td>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>2_0</td>
      <td>Aug 14, 2015</td>
      <td>Supported</td>
      <td>See below</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td>2_1</td>
      <td>July 15, 2017</td>
      <td>Supported</td>
      <td>See below</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td>2_2</td>
      <td>Jan 25, 2019</td>
      <td>Current version</td>
      <td>See below</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>

#### v1.4

The following fields have been added to the interface:
* Shipment/Content
* Shipment/CostCenter
* Shipment/CustomerOrderNumber
* Shipment/Remark
* Shipment/ReturnReference
* Shipment/ReturnBarcode
* Amount/BIC
* Amount/IBAN

The following fields have been removed from the interface:
* Amount/AccountNr

To comply with SEPA regulation, the bank account details must be entered in IBAN format. The COD card has been changed to print the IBAN bank account number.

#### v1.5

Different namespace

Note: due to changes in the backend the Label in the box (return label) functionality is only available from version 1_6 or later.

The following fields have been added to the interface:
* Shipment\ProductOption\Option
* Shipment\ProductOption\Characteristic
* Shipment\DeliveryDate
* Shipment\DeliveryAddress

#### v1.6

Different namespace

#### v1.7

The following field has been added to the interface:
* Shipment.DownPartnerLocation

#### v1.8

The following fields have been added to the interface:
* Shipment.IDNumber
* Shipment.IDType
* Shipment.IDExpiration
* Shipment.ReceiverDateOfBirth

The field StreetHouseNrExt is now usable for locations in NL, BE and DE.

#### v1.9

The request now includes a field for adding a signature to the labels generated by the service. This field is optional, so no change is required to use the new version of the service.

Shipment validation errors now include an error code in addition to the error message.

#### v2.0

Multiple shipments can now be sent in one request to the labelling service. To this end the Shipment field has been replaced by a Shipments field, which contains a list of Shipment elements. The response has also been modified. Instead of a ResponseShipment element, the response now consists of a GenerateLabelResponse element, which has a ResponseShipments field containing multiple ResponseShipment elements.

You can use this functionality with the GraphicFile|PDF|Merge printer types to generate one label document containing multiple labels. These “merged label” documents can be found in the new MergedLabels response field.

If you want to send only one shipment, you have to specify the Shipments element containing one Shipment.

#### v2.1

PostNL has implemented a commercial route to China. In order to do this, the following fields have been added to the interface:
* Shipment.Customs.Content.Content.EAN
* Shipment Customs.Content.Content.ProductURL

**NOTE: THIS PRODUCT NO LONGER EXIST**

The Shipment.Customs.Content element can occur up to 10 times instead of 5.
* DeliveryTimestampStart (Delivery on Demand label)
* DeliveryTimestampEnd (Delivery on Demand label)

**NOTE: THIS PRODUCT NO LONGER EXIST**

#### v2.2

The following fields have been added to the interface for shipments to the USA:
* Shipment.Customs.TrustedShipperID
* Shipment.Customs.ImporterReferenceCode
* Shipment.Customs.TransactionCode
* Shipment.Customs.TransactionDescription

A Codingtext have been added to the labels for mailbox parcels (brievenbuspakje)
* Shipment.CodingText (response)