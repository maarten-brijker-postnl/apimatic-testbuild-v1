# Product Codes

The PostNL Parcels API can be used with a variety of PostNL Pakketten shipping products. Each shipping product requires to be agreed upon in a contract between PostNL Pakketten and customers. The product codes mentioned must be used in various requests. The combilabel product codes are mapped to regular product codes.
    
Some specific product codes have different business rules which they need to comply with.

# Destination Netherlands

## Standard Dutch domestic

We distinguish these common products:

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3085</td>
      <td>Standard shipment</td>
    </tr>
    <tr>
      <td>
        <p>3385</p>
      </td>
      <td>
        <p>Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3090</p>
      </td>
      <td>
        <p>Delivery to neighbour + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3390</p>
      </td>
      <td>
        <p>Deliver&nbsp;to stated address only&nbsp;+ Return when not home</p>
      </td>
    </tr>
  </tbody>
</table>

**Business rules (__for all products__)**

* Receiver address fields required:<br>
  * Home number (only mandatory for Benelux shipments)<br>
  * Postcode (only mandatory for Benelux shipments)<br>
  * City<br>
  * Country code<br>
  * Street<br>
  * Last name/ Company name (at least one is required)
  
* Barcode requirements (not mandatory for Parcels non-EU labels):<br>
  * Type must be 3S<br>
  * Range must be 1-4 letter string<br>
  * Serie must be 7-12 digits<br>
  * Barcode must be 13-15 characters long<br>

## Extra cover

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3087</p>
      </td>
      <td>
        <p>Extra Cover</p>
      </td>
    </tr>
    <tr>
      <td>3094</td>
      <td>Extra cover + Return when not home</td>
    </tr>
  </tbody>
</table>

**Business rules**

* Insurance amount (type 02) is required. 
* Insurance amount entered cannot exceed the maximum allowed amount (€ 5000,-)

## Signature on delivery

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3089</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3096</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3189</p>
      </td>
      <td>
        <p>Signature on delivery</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3389</p>
      </td>
      <td>
        <p>Signature on delivery + Return when not home</p>
      </td>
    </tr>
  </tbody>
</table>

## Pickup points

With the delivery option Pickup, your customers can choose a pickup point to pick up their parcels.

More than 4000 pickup points available in supermarkets, bookstores etc.

It is mandatory to use the Checkout or the Location API to show he nearest PostNL Pickup points based on the postal code or coordinates of the customers. 

This frontend solution will return the correct information about the pickup point, which you will have to use in the Shipping, Labelling and/or Confirming API. Please check the specific documentation for more specific information.
    
Note:<br>
It is also possible to let your customers choose pickup points in Belgium. Please contact your PostNL accountmanager if you consider this option. For more information see the paragraph Pickup at PostNL Location Belgium.

Furthermore, in the Shipping, Labelling and/or Confirming API you will need to provide us with:
* the complete address of your customer
* the complete address of the pick up point

Confirming is essential for Pickup points shipments. Without an confirming on time, it is not possible to process these parcels.

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3533</p>
      </td>
      <td>
        <p>Pickup + Signature on Delivery</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3534</p>
      </td>
      <td>
        <p>Pickup + Extra Cover</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3543 *</p>
      </td>
      <td>
        <p>Pickup + Signature on Delivery + Notification</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3544 *</p>
      </td>
      <td>
        <p>Pickup + Extra Cover + Notification</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Parcels account manager.

**Business rules**
* Receiver address fields required:
  * Company name or last name
  * Street
  * Home number
  * Postcode
  * City
* Pickup point location address fields required:
  * Company name
  * Street
  * Home number
  * Postcode
  * City
* Receiver contact fields required (only for the product codes with Notification):
  * Email address or mobile phone number

## Mailbox parcel (brievenbuspakje)

With this product you will have the possibility to send a shipment that fits into the mailbox of your customers and have some shipping status information during the shipping process.

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>2928</p>
      </td>
      <td>
        <p>
          <span style="font-family: Calibri, sans-serif;">Mailbox parcel + Unsorted (ongesorteerd aanleveren)</span>
        </p>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>2929</p>
      </td>
      <td>
        <p>Mailbox parcel + Sorted (gesorteerd aanleveren)</p>
      </td>
    </tr>
  </tbody>
</table>

**Note:** It is not possible to sent multiple shipments of this product (Multicollo) in one request to the Shipping or Labelling webservice.

Please use the latest version of the Shipping | Labelling API because a required coding line is added to the Mailbox parcel label template.

**What is a coding line?**<br>
A coding line is a readable line of text, consisting of letters and numbers. It is printed on all postal items we process through our letter department and allows us to deliver your mail smarter and faster.

The coding line is based on parameters such as delivery date and address and therefore address-specific content of the coding line can change over time. To ensure its validity coding lines must be retrieved from an online PostNL solution. 

When the coding line has been successfully generated you will also see the Letter on the labels of the sorting center which you will need for productcode 2929 (BBP+ sorted).

**Why is a coding line important?**<br>
With a coding line, our machines and employees can prepare each postal item and ensure that it is sorted for the correct delivery area. By using a coding line, we’re able to deliver your mail smarter and faster.

**Proces**<br>
You can only generate coding lines if you add the DeliveryDate during the labelling phase. The DeliveryDate can be in the format date <dd-mm-yyyy> or in the format date+time <dd-mm-yyyy hh:mm:ss>. The date is mandatory, but you can choose whether you want to add the time as well.

For a correct DeliveryDate you can use the following day excluding Sunday and Monday.

Please use the exact same DeliveryDate during generating labels and confirmation.

**Error codes of the coding line (default coding lines)**<br>
Please make sure that single Coding text requests are made with a minimum interval of 200 milliseconds between service calls. Also make sure to complete this process at least 3 times before falling back to the default coding line. This way you get as many good coding lines as possible on the parcels.

**N0N coding line**

#000N0N#00#0000#

This default coding rule occurs if no proper coding rule is issued within the process before the labelling process continues.

**X0X coding line**

#0000X0X#00#0000#

This default coding rule can be caused by a foreign address, an address unknown (to PostNL), the presence of a PostNL service at that address (eg moving service) or an incorrect use of the DeliveryDate. If larger amounts of X0X coding rules are generated, it is often because the DeliveryDate is not correctly specified (see above).

## ID check

This product offers you the ability to make sure that confidential and age-validation transactions can be secure. So if you have some product(s) were identification or age control is required, it is possible to let the deliverer check the ID.

**Age validation**

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3438</td>
      <td>Standard shipment + Age Check</td>
    </tr>
    <tr>
      <td>3443</td>
      <td>Extra Cover + Age Check</td>
    </tr>
    <tr>
      <td>3446</td>
      <td>Extra Cover + Retun when not home + Age Check</td>
    </tr>
    <tr>
      <td>3449</td>
      <td>Retun when not home + Age Check</td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager.

Combine these product codes with the following product option: 

* product option: characteristic 002, option 014

We distinguish the following types:

<table>
  <thead>
    <tr>
      <th>Type</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>01</td>
      <td>Dutch residence document</td>
    </tr>
    <tr>
      <td>02</td>
      <td>Dutch ID</td>
    </tr>
    <tr>
      <td>03</td>
      <td>Dutch passport</td>
    </tr>
    <tr>
      <td>04</td>
      <td>Dutch driving license</td>
    </tr>
    <tr>
      <td>05</td>
      <td>European ID</td>
    </tr>
    <tr>
      <td>07</td>
      <td>Foreign ID</td>
    </tr>
  </tbody>
</table>

**Pickup Points (ID check)**

It is also possible to send the parcels to PostNL Pickup Points. Please note that you also must use the product options and business rules as described in the Pickup points paragraph. 

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3571</td>
      <td>Pickup + Age Check</td>
    </tr>
    <tr>
      <td>3574</td>
      <td>Pickup + Age Check + Notification</td>
    </tr>
    <tr>
      <td>3581</td>
      <td>Pickup + Extra Cover + Age Check</td>
    </tr>
    <tr>
      <td>3584</td>
      <td>Pickup + Extra Cover + Age Check + Notification</td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Parcels account manager.

ID Check products must be used in combination with a specific product option:

* Age validation requires product option: characteristic 002, option 014

## Registered letter labels

PostNL offers the possibility of sending registered mail items. This is called Registered letter labels. This offers you the ability to make sure that confidential and age-validation transactions can be secure. So if you have some letter(s) were identification or age control is required, it is possible to let the deliverer check the ID.

There are two possibilities:

* Registered letters (1010, 1011, 1020, 1410, 1420)

* ID check labels (1175)

These products can only be used after consulting your PostNL account manager.

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>1010, 1011*</p>
      </td>
      <td>
        <p>Registered letter</p>
      </td>
    </tr>
    <tr>
      <td>1020</td>
      <td>Registered parcels Losse Post</td>
    </tr>
    <tr>
      <td>1410</td>
      <td>Registered letters Partijen Post</td>
    </tr>
    <tr>
      <td>1420</td>
      <td>Registered parcels Partijen Post</td>
    </tr>
    <tr>
      <td>
        <p>1175</p>
      </td>
      <td>
        <p>Letter + ID check</p>
      </td>
    </tr>
  </tbody>
</table>

\* To be used in combination with franking machine.

## Dangerous goods

Offering dangerous goods (ADR shipments) with a statutory exemption, is only possible if a special business contract of carriage has been concluded with PostNL Pakketten. The transport of dangerous goods with a statutory exemption is permitted subject to certain conditions. Please contact your PostNL Pakketten account manager if you want to ship this goods. All the domestic product codes can be used in combination with dangerous goods, except the product codes for letters. The products can only be used after consulting your PostNL Pakketten account manager. 

Combine these product codes with the following product option:

* product option: characteristic 136, option 006

**Business rules**

* Product option and Characteristic are required. 
* Field Reference must be filled with ADR/LQ (possibly followed by your own customer reference)

## Pickup service

The Afhaalservice Basis and Plus (Pickup Basic and Plus) allows you to instruct a PostNL Parcels driver to go to a specific address on a specific date to retrieve (a) parcel(s). A maximum of 5 parcels can be collected per pick up, pick up requests with more than 5 parcels will be denied. The parcel(s) will then be delivered to an (antwoordnummer)address specified by you. The driver will provide the shipment label, so there is no option to create one via the API. For these products, the Confirming WebService must be used. For an example of a Pickup basic shipment, please refer to the Confirming WebService documentation.

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3151*</p>
      </td>
      <td>
        <p>Pickup Plus (collection order)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3160**</p>
      </td>
      <td>
        <p>Pickup Basic (collection order)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3238</p>
      </td>
      <td>
        <p>Pickup Plus (delivery order)</p>
      </td>
    </tr>
  </tbody>
</table>

\*If you use the Pickup Plus service you must use both product codes (3151 and 3238).     

\*\*If you use the Pickup Basic service you must use both product codes (3160 and 3238).

Pickup products have a specific structure different from regular parcels or Cargo shipments. Pickup products consist of two Shipments, the collection order and the delivery order. Both orders must be placed in a separate Shipment in the request. This means that a request for a pickup product will contain two Shipment segments. Please refer to the Confirming API documentation for an example of a pickup plus order and a pickup basic order.

Business rules (Customer)

* A customer with AddressType 02 is required.

Business rules (Shipment)
  
* A shipment with 
  * AddressType 04 (collection address)
  * 2S barcode
  * Product code 3151 (Plus) or 3160 (Basic).
  * CollectionTimeStampEnd
  * CollectionTimeStampStart

* A shipment with 
  * AddressType 01 (receiver address). For Pickup Basic (3160) an Antwoordnummer address is required.
  * 3S barcode. The 3S barcode should be exactly the same as the 2S barcode; the number of characters. But with 3S instead of 2S.
  * Product code 3238.
  * Maximum 5 parcels per pick up

* A GroupType with 
  * 2S barcode of the first shipment
  * Count 
  * Sequence

**Pickup Basic and Plus**<br>
Pickup plus products consist of two Shipments, the collection order and the delivery order. Both orders must be placed in a separate Shipment in the request. This means that a request for a pickup plus product will contain two Shipment segments. The below structure is required:

<table>
  <thead>
    <tr>
      <th>Pickup plus Confirming structure</th>
      <th>Pickup basic Confirming structure</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>Customer</p>
      </td>
      <td>
        <p>Customer</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>Message</p>
      </td>
      <td>
        <p>Message</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>Shipments</p>
      </td>
      <td>
        <p>Shipments</p>
      </td>
    </tr>
    <tr>
      <td>
        <p style="padding-left: 20px;">Shipment</p>
        <ul>
          <li>AddressType 04</li>
          <li>2S barcode</li>
          <li>CollectionTimeStampEnd</li>
          <li>CollectionTimeStampStart</li>
          <li>ProductCode 3151</li>
        </ul>
      </td>
      <td>
        <p style="padding-left: 20px;">Shipment</p>
        <ul>
          <li>AddressType 04</li>
          <li>2S barcode</li>
          <li>CollectionTimeStampEnd</li>
          <li>CollectionTimeStampStart</li>
          <li>ProductCode 3160</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <p style="padding-left: 20px;">Shipment</p>
        <ul>
          <li>AddressType 01</li>
          <li>3S barcode the same as 2S (but with 3S)</li>
          <li>Grouptype 01</li>
          <li>Mainbarcode 2S of first shipment</li>
          <li>GroupCount</li>
          <li>GroupSequence</li>
          <li>ProductCode 3238</li>
        </ul>
      </td>
      <td>
        <p style="padding-left: 20px;">Shipment</p>
        <ul>
          <li>AddressType 01
            <ul>
              <li>Antwoordnummer required</li>
            </ul>
          </li>
          <li>3S barcode the same as 2S (but with 3S)</li>
          <li>Grouptype 01</li>
          <li>Mainbarcode 2S of first shipment</li>
          <li>GroupCount</li>
          <li>GroupSequence</li>
          <li>ProductCode 3238</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Evening delivery

PostNL will deliver parcels on working days between 5.30 – 10.00 pm. It is mandatory to use the Checkout or delivery options API('s) of PostNL to let your customers choose an evening for the delivery. This frontend solution (Timeframe API) will return the correct information about the delivery, which you will have to use in the confirming and / or labelling service. For example: for evening delivery you will need product options. Please check the specific confirming and / or labelling documentation for more information.

You will need to provide us with the delivery date of the parcel. This delivery date will be checked in our database. We cannot provide evening delivery for all addresses in the Netherlands. Therefore, it is important to check if the stated delivery date and postal code are known in our database.

For evening delivery, confirming is essential. Without a confirming on time, it is not possible to process these parcels. Therefore, we strongly advise to use the method ‘generate label’ in the labelling service. Furthermore, you need to hand over the parcels one day before the delivery date. If you hand over the evening parcels too soon or too late, they will be delivered the next evening.

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3085 **</td>
      <td>Standard shipment</td>
    </tr>
    <tr>
      <td>
        <p>3087 **</p>
      </td>
      <td>
        <p>Extra cover</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3089 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>3090 **</td>
      <td>
        <p>Delivery to neighbour + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3094 **</p>
      </td>
      <td>
        <p>Extra cover + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3096 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>3189 **</td>
      <td>Signature on delivery</td>
    </tr>
    <tr>
      <td>
        <p>3385 **</p>
      </td>
      <td>
        <p>Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>3389 **</td>
      <td>Signature on delivery + Return when not home</td>
    </tr>
    <tr>
      <td>
        <p>3390 **</p>
      </td>
      <td>
        <p>Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager.

\*\*It is mandatory to use a combination of product code and a product option. The PostNL frontend will return this product option.

Combine these product codes with the following product option:

* product option: characteristic 118, option 006

**Business rules**

* Delivery date is required:
  * Evening delivery must be allowed on the given delivery date
* Receiver address fields required:
  * Company name or last name 
  * Street 
  * Home number 
  * Postcode 
  * City
* Evening delivery must be allowed on the address specified
  * Receiver contact mobile or email is required

## Sunday delivery

PostNL will deliver parcels on Sundays between 10:00 -20:00 pm.

You will need to provide us with the delivery date of the parcel. This delivery date will be checked in our database. We cannot provide Sunday delivery for all addresses in the Netherlands. Therefore, it is important to check if the stated delivery date and postal code are known in our database. 

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3085 **</p>
      </td>
      <td>
        <p>Standard shipment</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3087 **</p>
      </td>
      <td>
        <p>Extra cover</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3089 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3094 **</p>
      </td>
      <td>
        <p>Extra cover + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3096 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3385 **</p>
      </td>
      <td>
        <p>Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3390 **</p>
      </td>
      <td>
        <p>Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager

\*\*It is mandatory to use a combination of product code and a product option.

Combine these product codes with the following product option: 

* product option: characteristic 101, option 008

**Business rules**

* Delivery date is required:
  * Sunday delivery must be allowed on the given delivery date
* Receiver address fields required
  * Company name or last name
  * Street
  * Home number
  * Postcode
  * City
* Sunday delivery must be allowed on the address specified

## Today delivery

PostNL Parcels offers the possibility to hand over parcels to PostNL on working days between 05.00 and 11.00 AM. These parcels will be delivered on the same evening (note: only working days Monday to Friday) between 5.30 PM and 10.00 PM. It is mandatory to retrieve availability of a given address for Today delivery using the Checkout or delivery options API('s).  a front-end solution (webservice). Please consult the documentation and business rules for more information about the front-end solutions.   

Confirming the Today delivery is essential. When using the PostNL Shipping or Labelling API to confirm shipments, a shipment is confirmed by default. In the situation that you override this setting with confirm=false in the URL (I.e. only requesting a label), confirming the shipment separately via the PostNL Confirming API is necessary. 
  
Without a confirmation before 10AM on day of handover to PostNL, it is not possible to process these parcels in time. 
  
Furthermore, parcels need to be handed over between 05.00 and 11.00 AM at the specified  location for Today. If Today parcels are handed over to the wrong location, they will be delivered the next day at the first available delivery moment.

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3085 **</td>
      <td>Standard shipment</td>
    </tr>
    <tr>
      <td>
        <p>3087 **</p>
      </td>
      <td>
        <p>Extra cover</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3089 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>3090 **</td>
      <td>
        <p>Delivery to neighbour + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3094 **</p>
      </td>
      <td>
        <p>Extra cover + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3096 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>3189 **</td>
      <td>Signature on delivery</td>
    </tr>
    <tr>
      <td>
        <p>3385 **</p>
      </td>
      <td>
        <p>Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>3389 **</td>
      <td>Signature on delivery + Return when not home</td>
    </tr>
    <tr>
      <td>
        <p>3390 **</p>
      </td>
      <td>
        <p>Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager

\*\*It is mandatory to use a combination of product code and a product option ‘Today’. Using ‘Today’ in combination with other product codes is not possible.

Combine these product codes with the following product option:

* product option: characteristic 118, option 044

**Business rules**

* Availability of Today delivery on given address must be allowed and confirmed by using the DeliveryDate + Timeframe webservice OR Checkout webservice. 
* Confirmation must be received by PostNL before 10.00AM on the day of handover to PostNL.
* Confirmation for Today delivery must contain:
  * Today product option code: characteristic 118, option 044
  * Delivery date
  * Receiver address fields: Company name or last name, Street name, House number, Postcode
  * Receiver contact mobile phone number or email addres

## Sameday delivery

PostNL Parcels offers the possibility to deliver parcels on the same day if customer order before lunchtime*. PostNL will deliver parcels on working days between 5.30 – 10.00 pm. We cannot provide same day delivery for all addresses in the Netherlands; therefore, it is important to check if the postal codes are known in our database and allow evening/ same day delivery. This can be done by using the Timeframe API.

\*This is a indicative time; for the exact time please contact your PostNL Pakketten account manager.

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3085 **</td>
      <td>Standard shipment</td>
    </tr>
    <tr>
      <td>
        <p>3087 **</p>
      </td>
      <td>
        <p>Extra cover</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3089 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>3090 **</td>
      <td>
        <p>Delivery to neighbour + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3094 **</p>
      </td>
      <td>
        <p>Extra cover + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3096 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>3189 **</td>
      <td>Signature on delivery</td>
    </tr>
    <tr>
      <td>
        <p>3385 **</p>
      </td>
      <td>
        <p>Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>3389 **</td>
      <td>Signature on delivery + Return when not home</td>
    </tr>
    <tr>
      <td>
        <p>3390 **</p>
      </td>
      <td>
        <p>Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager

\*\*It is mandatory to use a combination of product code and a product option.

Combine these product codes with the following product options (both product options are needed for this product):

* product option: characteristic 118, option 015
* product option: characteristic 118, option 006

**Business rules**

* Delivery date is required:
  * Sameday delivery must be allowed on the given delivery date
* Receiver address fields required:
  * Company name or last name
  * Street
  * Home number
  * Postcode
* Receiver contact mobile phone number or email address
  * Sameday delivery must be allowed on the address specified (use the timeframe webservice)

## Guaranteed / morning delivery

If your customer needs the parcel the next day as soon as possible and/or guaranteed, then you can use the product guaranteed delivery. 

There are four options: 

* Early morning. On working days before 09:00. 
* Morning. On working days before 10:00. 
* Noon. On working days before 12:00.
* Afternoon. On working days before 17:00. 

If the service has not been carried out according to our promises, you can request a reimbursement of the surcharge. Ideal for recipients who need certainty on their shipment. 

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3085 **</p>
      </td>
      <td>
        <p>Standard shipment</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3087 **</p>
      </td>
      <td>
        <p>Extra cover</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3089 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3090 **</p>
      </td>
      <td>
        <p>Delivery to neighbour + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3094 **</p>
      </td>
      <td>
        <p>Extra cover + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3096 **</p>
      </td>
      <td>
        <p>Signature on delivery + Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3189 **</p>
      </td>
      <td>
        <p>Signature on delivery</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3385 **</p>
      </td>
      <td>
        <p>Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3389 **</p>
      </td>
      <td>
        <p>Signature on delivery + Return when not home</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3390 **</p>
      </td>
      <td>
        <p>Deliver to stated address only + Return when not home</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager

\*\*It is mandatory to use a combination of product code and a product option.

Combine these product codes with one of the following product options: 

* product option: characteristic 118, option 017 (delivery before 09:00) 
* product option: characteristic 118, option 007 (delivery before 10:00) 
* product option: characteristic 118, option 008 (delivery before 12:00) 
* product option: characteristic 118, option 012 (delivery before 17:00)

**Business rules**

* Delivery date is required
  * Guaranteed delivery must be allowed on the given delivery date
* Receiver address field required:
  * Street 
  * Home number 
  * Postcode 
  * City
* Guaranteed delivery must be allowed on the address specified
* Receiver contact mobile phone number or email address is required. 

## Instant / on demand bike delivery

Note: Due to the fact that in some cases another connection is required for this product. It is important to contact your PostNL accountmanager or partnermanager before implementing this product.

With the service ‘Instant/ On demand Bike Delivery’ you can book instant, within 2-hour delivery or 2 hour timeslots delivery to consumers in designated service areas within cities. The receiver can choose a timeframe of two hours themselves in the checkout of the webshop, when he/she wishes to receive the parcel, the first time slot starting at the first 15 minute interval available and ending 2 hours after the start of that timeframe (E.a. 13.15 - 13.30 - 13.45 - 14.00) During the delivery, the consumer will receive extra push notifications via e-mail with confirmation of order, confirmation of pick-up and confirmation of delivery. This way, the consumer is even better in control of receiving the parcel.

PostNL delivers the parcels from Monday to Friday in the chosen timeframe (two hours between 12:00-20:00 h).

This service is locally and only on request available in certain cities in the Netherlands (Amsterdam, Utrecht, Rotterdam, The Hague, Eindhoven). The zip codes are user specific and managed by the customer. Postal codes of every pick-up location have to be shared with PostNL and you will receive a service area specifically for each pick-up location. Every order must be checked in combination with the desired delivery area.

Before booking an order there must have been a confirmation at the pick-up location that the requested order is available on the location and that the location is going to be able to pick, package and label every order individually at a maximum of 15 minutes after the start of the requested pick-up slot.

When an address is not attainable in the chosen timeframe, for example in (traffic) situations and circumstances beyond the control of PostNL, PostNL cannot be held responsible failing in delivery within the chosen timeframe. The receiver of the parcel is responsible to choose a timeframe when its address is attainable.

This timeframe option can be combined with the following products:

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3070**</p>
      </td>
      <td>
        <p>Instant delivery</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager.

\*\*It is mandatory to use a combination of product code and a product option. The PostNL frontend will return this product option.

Combine these products with on of the following product options:

* product option: characteristic 118, option 032
* product option: characteristic 152, option 025

**Business rules**

* DeliveryTimeStampEnd and DeliveryTimeStampStart are required. This fields should contain the timeframe retrieved from the Timeframe webservice response.
* Delivery date is required.
* Sender address field is required:
  * Street
  * Home number
  * Postalcode
  * City
* Receiver address field required:
  * Street
  * Home number
  * Postalcode
  * City
* Max. dimensions is 60x60x40 cm
* Max. amount of parcels in one shipment: 2
* Max. total weight is 15KG
* Receiver contact fields required
* Email address is obligatory and mobile phone number is optional

# Destination Netherlands (from Belgium)

We distinguish these common products:

<table>
    <thead>
        <tr>
            <th>Product Code*</th>
            <th>Service description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>4890</td>
            <td>Standard shipment </td>
        </tr>
        <tr>
            <td>4891</td>
            <td>Signature on delivery </td>
        </tr>
        <tr>
            <td>4893</td>
            <td>Delivery to stated address only</td>
        </tr>
        <tr>
            <td>4894</td>
            <td>Signature on delivery + Delivery to stated address only </td>
        </tr>
        <tr>
            <td>4895****</td>
            <td>Age check 18+ + Delivery to stated address only </td>
        </tr>
        <tr>
            <td>4896</td>
            <td>Signature on delivery, Delivery to stated address only, Return when not home </td>
        </tr>
        <tr>
            <td>4897**</td>
            <td>Extra cover </td>
        </tr>
        <tr>
            <td>4898***</td>
            <td>Pickup at PostNL location, Signature on delivery </td>
        </tr>
    </tbody>
</table>

\* All Parcels EU products include standard signature on delivery and standard coverage of €500,-.

\*\* Business rule Insurance amount (type 02) is required and cannot exceed the maximum allowed amount (€ 5000,-). Please find more detailed specifications in the corresponding Shipping, Confirming and Labelling webservices documentation. 

\*\*\* It is possible to let your customers choose pick up points. It is mandatory to use a delivery option (Location or Checkout API) solution to let your customer choose a pick up point. 

\*\*\*\* Combine these product codes with the following product option: <br>
    - product option: characteristic 002, option 014

Please note: if you send parcels to other EU destinations with Parcels EU codes, you can still use these codes for EU destinations other than Belgium. 


# Destination Belgium

## Belgium domestic

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>4960</p>
      </td>
      <td>
        <p>Belgium Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4961</p>
      </td>
      <td>
        <p>Belgium Delivery to neighbour</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4962</p>
      </td>
      <td>
        <p>Belgium Signature on delivery + Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4963</p>
      </td>
      <td>
        <p>Belgium Signature on delivery</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4965 **</p>
      </td>
      <td>
        <p>Belgium Extra cover (EUR 500) + Deliver to stated address only</p>
      </td>
    </tr>
  </tbody>
</table>

\* Can only be used after consulting your PostNL Parcels account manager. 

\*\* Business rule Insurance amount (type 02) is required and cannot exceed the maximum allowed amount (€ 5000,-). Please find more detailed specifications in the corresponding Shipping, Confirming and Labelling webservices documentation.

## Pickup at PostNL location Belgium

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>4878 **</p>
      </td>
      <td>
        <p>Pickup at PostNL Location Belgium insured.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4880</p>
      </td>
      <td>
        <p>Pickup at PostNL Location Belgium, no insurance.</p>
      </td>
    </tr>
  </tbody>
</table>

\*Can only be used after consulting your PostNL Pakketten account manager.

\*\* Business rule Insurance amount (type 02) is required and cannot exceed the maximum allowed amount (€ 5000,-). Please find more detailed specifications in the corresponding Shipping, Confirming and Labelling webservices documentation.

It is possible to let your customers choose pick up points in Belgium. It is mandatory to use a frontend solution to let your customer choose a pick up point. See for more information the paragraph Pickup Points (Dutch domestic products). 

**Business rules**

* Downnetwork partner ID is required
* Downnetwork pickup location code is required
* Address type 09 is required (partner pickup location), please refer to the LocationWebService to retrieve the correct pickup location addresses

## Netherlands to Belgium

Standard delivery to Belgium.<br>
Please be aware: these products need to be added to your contract before using them. Contact your PostNL Pakketten accountmanager in order to check if additional action is needed.

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>4936</p>
      </td>
      <td>
        <p>Pick up at a PostNL location in Belgium**</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4941</p>
      </td>
      <td>
        <p>Deliver to stated address only</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4946</p>
      </td>
      <td>Belgium Standard delivery</td>
    </tr>
    <tr>
      <td>
        <p>4912</p>
      </td>
      <td>
        <p>Parcel Netherlands-Belgium + Signature upon delivery</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4914</p>
      </td>
      <td>
        <p>Parcel Netherlands-Belgium + extra cover***</p>
      </td>
    </tr>
  </tbody>
</table>

\* Can only be used after consulting your PostNL Parcels account manager. 

\*\* It is possible to let your customers choose pickup points in Belgium. It is mandatory to use a front-end solution to let your customer choose a pickup point. See for more information the paragraph Pickup Points (Dutch domestic products).

\*\*\* Business rules Insurance amount (type 02) is required and cannot exceed the maximum allowed amount (€ 5000,-)

## Return label

PostNL offers the possibility to create returns labels for Belgium.<br>
You can request return labels in the same two ways for Dutch domestic return shipments (Label in the box and a single label). You can request a return label directly, or you can request a return label with your regular shipping label (label in the box). Both examples are shown below.

**Single label variant**<br>
The return labels for Belgium require some specific fields to be used:

* address of receiver: Shipment/Address/AddressType 01
* address of sender: Customer/Address/AddressType 02
* Countrycode: BE
* Product code: dependent on the origin country. If your company is located in the Netherlands, you must use product code 3250. If your company is located in Belgium you must use product code 4882 for domestic returns and product code 4785 for return from the Netherlands back to Belgium.

**Label in the box**<br>
For the label in the box variant, you adjust your regular shipping label API call with some extra parameters. This results in an output of two labels, one initial shipping label and one return label.Label in the box return labels require some specific fields to be used:

* Address of receiver: Shipment/Address/AddressType 01
* Address of sender: Customer/Address/AddressType 02
* Return address: Shipment/Address/AddressType 08
* Product code: regular product codes
* Return barcode: Shipment/ReturnBarcode

For the return process in Belgium, a printed label on the box is required. Labels can not be printed within the PostNL pick-up points.

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>- *</p>
      </td>
      <td>
        <p>Label in the box</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3250 **</p>
      </td>
      <td>
        <p>Single label variant (when your company is located in the Netherlands)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>4882 **</p>
      </td>
      <td>
        <p>Single label variant&nbsp;(when your company is located in Belgium)</p>
      </td>
    </tr>
  </tbody>
</table>

\*No separate product code, created your return label at the same moment as you create the shipment label.

\*\*These product codes can only be used after consulting your PostNL Pakketten account manager.

**Business rules**<br>
Address type 1 Contact fields required: Email address \*

\*To receive a digital confirmation of handing over the parcel to PostNL.

# Destination EU

## Parcels EU

<table>
  <thead>
    <tr>
      <th>Product and service</th>
      <th>Product code delivery</th>
      <th>Characteristic & Option I</th>
      <th>Characteristic & Option II</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Parcel EU 2C Track & Trace</td>
      <td>4907</td>
      <td>005-025</td>
      <td>101-012</td>
    </tr>
    <tr>
      <td>Parcel EU 2C Track & Trace Insured</td>
      <td>4907</td>
      <td>004-015</td>
      <td>101-012</td>
    </tr>
    <tr>
      <td>Parcel EU 2C Track & Trace Insured Plus</td>
      <td>4907</td>
      <td>004-016</td>
      <td>101-012</td>
    </tr>
    <tr>
      <td>Parcel EU 2B Track & Trace</td>
      <td>4907</td>
      <td>005-025</td>
      <td>101-013</td>
    </tr>
    <tr>
      <td>Parcel EU 2B Track & Trace Insured</td>
      <td>4907</td>
      <td>004-015</td>
      <td>101-013</td>
    </tr>
    <tr>
      <td>Parcel EU 2B Track & Trace Insured Plus</td>
      <td>4907</td>
      <td>004-016</td>
      <td>101-013</td>
    </tr>
    <tr>
      <td>Parcel EU Standard*</td>
      <td>4999</td>
      <td></td>
      <td></td>
    </tr>
  </tbody>
</table>

Product codes 4940, 4944, 4950 and 4952 can still be used for the Parcel EU product until further notice.

\* This product code is only available for destination France and can only be used after consulting your PostNL account manager. 

Per  the 1st of January 2023 we renewed our International Parcel portfolio . In order to profit from our new international services, we ask you to adjust the way of pre-alerting. Instructions are available <a href="https://developer.postnl.nl/internationalservices/" target="_blank" rel="noopener noreferrer">here</a>.
Parcel EU shipments are available ‘2C’ recipient is a consumer or ‘2B’ recipient is a business. Next to this there are three services available:

* A Parcel Track & trace is a parcel with track & trace. 
* A Parcel Track & trace insured is a parcel with track & trace, proof of delivery and insured up to €50,-
* A Parcel Track & Trace Insured Plus is a parcel with track & trace, proof of delivery and insured up to €500,-. 

Read more about our <a href="https://www.postnl.nl/zakelijke-oplossingen/pakket-versturen/pakket-buitenland/" target="_blank" rel="noopener noreferrer">international parcel solutions</a>.

For an example API message of this product, view our example messages in the postman collection.

The barcode type for the above barcodes is 3S and the barcode length contains 13 characters. PostNL automatically provides you with the correct shipping label. Track & trace and billing for all parcel EU shipments are based on the 3S barcode.

Parcel EU is available to the following destinations: AT, BG, HR, CY, DK (1), EE, FI, FR (2), DE, SI, GR, HU, IE, IT (3), LV, LT, LU, MT, CZ, PL, PT (4), RO, SK, ES (5), SE

1. Excluding Faroe Islands and Greenland 
2. Including Monaco and Corsica. Excluding Andorra 
3. Excluding San Marino and Vatican City 
4. Including Azores and Madeira 
5. Including Balearic Islands. Excluding Canary Islands, Melilla and Ceuta

To recognize the Canary Islands (5):

Las Palmas has country code IC and zip codes start with 35. Santa Cruz has country code IC and zip codes start with 38. Melilla has country code EA and zip code starts with 52.

Parcels to the Canary Islands can only be sent with the Parcels non-EU product: Ask your account manager about the available options.

**Business rules**

* Barcode requirements
  * Type must be 3S 
  * Range must be 1-4 letter string 
  * Serie must be 7-12 digits 
  * Barcode must be 13 characters long
* Receiver country must be a Parcels EU country 
* Receiver address fields required
  * Company name or last name 
  * City 
  * Country code

## Easy Return Service (ERS)

With this product you give your customers the opportunity to return shipments from abroad up to 30kg free of charge. Items can be sent back to The Netherlands via a nearby local post office in all EU countries and some Non-EU countries. Parcels are fully traceable.  

Check the <a href="https://www.postnl.nl/zakelijke-oplossingen/pakket-versturen/retouren/internationale-retouren/" target="_blank" rel="noopener noreferrer">PostNL site</a> for more information and the countries where this service can be used.

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4910</td>
      <td>Easy Return Service, via PostNL directly returned to the customer</td>
    </tr>
    <tr>
      <td>4911*</td>
      <td>Easy Return Service, consolidated by PostNL and returned to the customer</td>
    </tr>
    <tr>
      <td>4915*</td>
      <td>Commercial Returns, consolidated by PostNL and returned to the customer (note only possible for returns from BE, DE, FR)</td>
    </tr>
  </tbody>
</table>

\* This product code is only available after consulting your PostNL account manager. 
You have to use the Shipping v1 or Labelling 2.2 API for this product. 
The API is easy to use if you want to request return labels in advance for your customer so you can include them in the box.  Customers can immediately use the return label by simply affixing it on the parcel and handing it over at a local post office.  
If you want more control over your returns, you can also make use of the Return portal. Via the Return portal it is easy to request a label which you can share with your customer. Customers can even request the labels themselves and also indicate the reason for their return.  

Note: The output is .pdf. It is not possible to create a .zpl format label. 

**Business rules**  

* Receiver contact email address is required.
* Barcode requirements: 
  * Type must be 3S and a barcode of Postal operator 
* Return address in The Netherlands  

## International Business Reply Service (IBRS)

With this product you give your customers the opportunity to return lightweight shipments up to 2kg free of charge. This can be sent back to The Netherlands via a nearby local post office. 

Check the <a href="https://www.postnl.nl/zakelijke-oplossingen/pakket-versturen/retouren/internationale-retouren/" target="_blank" rel="noopener noreferrer">PostNL site</a> for more information and the countries where this service can be used.

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2484</td>
      <td>IBRS</td>
    </tr>
  </tbody>
</table>

Note: The output is .pdf. It is not possible to create a .zpl format label. 

**Business rules**  
* Business reply number in The Netherlands 

# Destination Rest Of World

## Parcels Non-EU

<table>
  <thead>
    <tr>
      <th>Product and service</th>
      <th>Product code delivery</th>
      <th>Characteristic & Option</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Parcel Non EU Track & Trace</td>
      <td>4909</td>
      <td>005-025</td>
    </tr>
    <tr>
      <td>Parcel Non EU Track & Trace Insured</td>
      <td>4909</td>
      <td>004-015</td>
    </tr>
    <tr>
      <td>Parcel Non EU Track & Trace Insured Plus</td>
      <td>4909</td>
      <td>004-016</td>
    </tr>
  </tbody>
</table>

Product codes 4945 and 4947 can still be used for the Parcel Non-EU product until further notice.  Please note for destination UK (DDP) and US (DDU) we also have specific solutions.

Per  the 1st of January 2023 we renewed our International Parcel portfolio . In order to profit from our new international services, we ask you to adjust the way of pre-alerting. Instructions are available <a href="https://developer.postnl.nl/internationalservices/" target="_blank" rel="noopener noreferrer">here</a>.

For Parcel Non-EU there are three services available:

*  A Parcel Track & trace is a parcel with track & trace. 
*  A Parcel Track & trace insured is a parcel with track & trace, proof of delivery and insured up to €50,-. 
*  A Parcel Track & Trace Insured Plus is a parcel with track & trace, proof of delivery and insured up to €500,-.

Read more about our <a href="https://www.postnl.nl/zakelijke-oplossingen/pakket-versturen/pakket-buitenland/" target="_blank" rel="noopener noreferrer">international parcel solutions</a>.

For an example API message of this product, view our example messages in the Postman collection.

The barcode type for the above products is a single internationally recognized S10 barcode and the barcode length contains 13 characters. Parcels non-EU S10 barcodes can only be generated via the API, using the Barcode method. Details are mentioned in the Barcode Webservice documentation.

PostNL automatically provides you with the correct shipping label. Track & trace and billing for all parcel Non EU shipments are based on the S10 barcode. The labels are printed on A5 paper (two or three forms A4, depending on the type of goods shipped).

**Country codes**

Parcels non-EU covers all countries except for the countries as mentioned in previous and Dutch/Belgium domestic sections. Please be aware of the specific exceptions as mentioned in the Parcels EU section.

**Business rules**

* Receiver address fields required
  * Company name or last name 
  * City 
  * Country code
* Parcels non-EU product code
  * Barcode type must be S10  
  * Either receiver or sender country code must not be an Parcels EU country 
  * Customs segment 
  * For shipments to the USA the contact segment must contain either a phone number or an e-mail address.
  * At least one Content segment 
  * Shipment type (the following types are possible: Documents, Commercial Sample, Commercial Goods, Returned Goods)
  * You must use the field “HandleAsNonDeliverable” with the value “false”.
    
## US Delivery Duty Unpaid (US DDU)

With the PostNL commercial solution customers have the benefit of a very fast transit time (3-5 working days) when shipping parcels to the US. This product is only available to customers with a specific contract for this solution. Please contact your PostNL account manager if you consider this option.

For regular postal parcels to the US via USPS our non-EU product (product code 4945) can be used.
  
This product is only available on our Shipping V1 and Labelling API version 2.2.

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Combilabel</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4905*</td>
      <td>Yes</td>
      <td>DDU Delivery Duty Unpaid</td>
    </tr>
  </tbody>
</table>

As the US is a non-EU destination mostly the same input is required as for our regular non-EU shipment.  Furthermore you will need to provide us with the following:

* At ‘ProductCodeDelivery’  product code ‘4905’ must be entered.
* A specific (new) customer number and customer code are required for this solution. These are supplied by PostNL. 
* It’s not needed to supply a S10 barcode a 3S barcode is sufficient which is requested via our barcode API
* At the contacts segment it’s mandatory to fill in: “Email” as this is used by our partner to send shipment updates.
* “SMSNr” and  “TelNr” are strongly advised and also used to send shipment updates to your customer. Be aware that when a number is supplied it’s mandatory to include an American telephone number which should include the country number and area code. 
* Only works for recipient country code ‘US’

Optional fields:

* “Reference” 
* “Remark” (can be used for a customer specific reference and is shown on the label output)

Output:

* Barcode: PostNL barcode which was already in the labelrequest)
* DownPartnerID: UPS-01/SAVER/DDU (partner abroad for delivery in US)
* DownPartnerBarcode: (barcode from partner abroad )
* One label is supplied in a Base64 string:
  * Labeltype = Label (combilabel, size  105mm x 148mm, A6)

**FULL DETAILS**

**Invoice**

Supplying a commercial Invoice with the parcel is not needed as an electronic commercial invoice is automatically generated based on the filled in values in the customs segment of the label request.

**Deviant fields in the API**

Since this product is a collaboration between PostNL and our partner abroad, some fields in our API are restricted to a max number of characters which differ from the amount of characters normally accepted by PostNL. Please note the following. 

<table>
  <thead>
    <tr>
      <th>PostNL API fieldname</th>
      <th>Max length</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>TelNr</td>
      <td>15</td>
    </tr>
    <tr>
      <td>SMSNr</td>
      <td>15</td>
    </tr>
    <tr>
      <td>Email</td>
      <td>35</td>
    </tr>
    <tr>
      <td>Reference</td>
      <td>35</td>
    </tr>
    <tr>
      <td>Remark</td>
      <td>35</td>
    </tr>
    <tr>
      <td>Name/CompanyName</p>(only use one)</td>
      <td>35</td>
    </tr>
    <tr>
      <td>Street + HouseNr + HouseNrExt</p>(all together mustn&rsquo;t exceed the limit)</td>
      <td>35</td>
    </tr>
    <tr>
      <td>Buildingname + Department</p>(all together mustn&rsquo;t exceed the limit)</td>
      <td>35</td>
    </tr>
    <tr>
      <td>City</td>
      <td>30</td>
    </tr>
    <tr>
      <td>Zipcode</td>
      <td>9</td>
    </tr>
    <tr>
      <td>HSTariffNr</td>
      <td>Min 6 - Max 10</td>
    </tr>
  </tbody>
</table>

Some fields which are normally supported in our API are not supported for this product, so make sure not to use the following fields.

* Department
* Floor
* Doorcode
* Area
* Region

In case of questions please consult your PostNL IT consultant.

## UK Delivery Duty Paid (UK DDP)

  With the PostNL commercial solution to ship parcels to United Kingdom*, as a result of the Brexit, the import duties are paid directly to PostNL by the customer. This way the recipient of the parcel doesn’t have to pay (unexpected) duties. This product is only available to customers with a specific contract for this solution. Please contact your PostNL account manager if you consider this option.

\*Northern Ireland and the British Channel Islands are also supported, please note transit time is increased with 2 days for these destinations.<br>
This product is only available on our Shipping V1 and Labelling API version 2.2

<table>
  <thead>
    <tr>
      <th>Product code</th>
      <th>Combilabel</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>4905*</p>
      </td>
      <td>
        <p>Yes</p>
      </td>
      <td>Delivery Duty Paid UK (DDP UK)</td>
    </tr>
  </tbody>
</table>

As United Kingdom is a non-EU destination mostly the same input is required as for our regular non-EU shipment.  Furthermore you will need to provide us with the following:

Input:

* At ‘ProductCodeDelivery’  product code ‘4905’ must be entered.
* A specific (new) customer number and customer code are required for this solution. These are supplied by PostNL. 
* It’s not needed to supply a S10 barcode a 3S barcode is sufficient which is requested via our barcode API
* It’s mandatory to fill in the ‘TrustedShipperId’ field. It should contain the British VAT number of the customer. 
* It’s mandatory to fill in the ‘ImporterReferenceCode’ field. It should contain the British EORI number of the customer. 
* At the contacts segment it’s mandatory to fill in: “Email” This is used to share tracking updates with your customer.
* Only works for recipient country code ‘GB’

Optional:

* ‘Reference’ (can be used for a customer specific reference and is shown on the label output)
* Remark’ (can be used for a customer specific reference and is shown on the label output)

Output:

* Barcode: PostNL barcode which was already in the labelrequest)
* DownPartnerID: HERMES/24/B2C  (partner abroad for delivery in UK)
* DownPartnerBarcode: (barcode from partner abroad)
* Two documents are supplied in the Base64 string:
  * Labeltype = Label (combilabel, size  105mm x 148mm, A6)
  * Labeltype = CommercialInvoice (size 210mm x 297mm, A4)

When choosing Printertype ‘GraphicFile|PDF|Merge’ the output of the Labetype will be ‘Label’. Both the label (A6) and Commercial Invoice (A4) will be in the same document.
  
**FULL DETAILS**

**Invoice**<br>
Supplying a commercial Invoice with the parcel is strongly adviced. We supply a commercial invoice via our API, but you may also use one of your own. If you supply parcels without a commercial invoice, make sure you always have one available in case of enquiries from customs.

**Deviant fields in the API**<br>
Since this product is a collaboration between PostNL and our partner, some fields in our API are restricted to a max number of characters which differ from the amount of characters normally accepted by PostNL. Please note the following.

<table>
  <thead>
    <tr>
      <th>PostNL API fieldname</th>
      <th>Max length</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>TelNr</td>
      <td>15</td>
    </tr>
    <tr>
      <td>TelNr</td>
      <td>15</td>
    </tr>
    <tr>
      <td>SMSNr</td>
      <td>15</td>
    </tr>
    <tr>
      <td>Email</td>
      <td>80</td>
    </tr>
    <tr>
      <td>Reference</td>
      <td>20</td>
    </tr>
    <tr>
      <td>Remark</td>
      <td>20</td>
    </tr>
    <tr>
      <td>FirstName</td>
      <td>50</td>
    </tr>
    <tr>
      <td>Name</td>
      <td>50</td>
    </tr>
    <tr>
      <td>HouseNr + HouseNrExt</td>
      <td>10</td>
    </tr>
    <tr>
      <td>Buildingname</td>
      <td>32</td>
    </tr>
    <tr>
      <td>Street</td>
      <td>50</td>
    </tr>
    <tr>
      <td>CompanyName + Department</td>
      <td>50</td>
    </tr>
    <tr>
      <td>Floor</td>
      <td>50</td>
    </tr>
    <tr>
      <td>Area</td>
      <td>50</td>
    </tr>
    <tr>
      <td>City</td>
      <td>32</td>
    </tr>
    <tr>
      <td>Region</td>
      <td>32</td>
    </tr>
    <tr>
      <td>Zipcode</td>
      <td>10</td>
    </tr>
    <tr>
      <td>CountryCode</td>
      <td>2</td>
    </tr>
  </tbody>
</table>

In case of questions please consult your PostNL IT consultant.

# International Mail & Packets

<table>
  <thead>
    <tr>
      <th>Service</th>
      <th>Product code</th>
      <th>Product name</th>
      <th>Required barcode type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Untracked</td>
      <td>6440</td>
      <td>Boxable Untracked</td>
      <td>UE</td>
    </tr>
    <tr>
      <td>Untracked</td>
      <td>6405</td>
      <td>Packet Untracked</td>
      <td>UE</td>
    </tr>
    <tr>
      <td>Untracked</td>
      <td>6945*</td>
      <td>Boxable Untracked (contract)</td>
      <td>UE</td>
    </tr>
    <tr>
      <td>Untracked</td>
      <td>6905*</td>
      <td>Packet Untracked (contract)</td>
      <td>UE</td>
    </tr>
    <tr>
      <td>Tracked</td>
      <td>6972</td>
      <td>Boxable Track & Trace</td>
      <td>LA</td>
    </tr>
    <tr>
      <td>Tracked</td>
      <td>6350</td>
      <td>Packet Track & Trace</td>
      <td>LA</td>
    </tr>
    <tr>
      <td>Tracked</td>
      <td>6942*</td>
      <td>Boxable Track & Trace (contract)</td>
      <td>LA</td>
    </tr>
    <tr>
      <td>Tracked</td>
      <td>6550*</td>
      <td>Packet Track & Trace (contract)</td>
      <td>LA</td>
    </tr>
    <tr>
      <td>Registered</td>
      <td>6906</td>
      <td>Packet Track & Trace insured</td>
      <td>RI</td>
    </tr>
    <tr>
      <td>Registered</td>
      <td>6908*</td>
      <td>Packet Track & Trace insured (contract)</td>
      <td>RI</td>
    </tr>
    <tr>
      <td>Registered</td>
      <td>6408</td>
      <td>Registered Letter</td>
      <td>RI</td>
    </tr>
    <tr>
      <td>Registered</td>
      <td>6605*</td>
      <td>Registered Bulk Mail</td>
      <td>RI</td>
    </tr>
  </tbody>
</table>

\* These product codes can only be used after consulting your PostNL account manager.

Per  the 1st of January 2023 we renewed our International portfolio . 

For (letterbox)packets three services are available:

*  A (letterbox)packet Basic is a packet without extra services  
*  A (letterbox)packet Track & trace is a packet with Track&Trace.
*  A Packet Track & Trace Insured is a packet with track&trace, proof of delivery and insured up to €50,-.

Read more about our <a href="https://www.postnl.nl/zakelijke-oplossingen/pakket-versturen/pakket-buitenland/pakjes-buitenland/" target="_blank" rel="noopener noreferrer">international parcel solutions</a>.

For an example API message of this product, view our example messages in the postman collection.

The barcode type for the above products is a single internationally recognized S10 barcode and the barcode length contains 13 characters. S10 barcodes can only be generated via the API, using the Barcode method. Details are mentioned in the Barcode Webservice documentation.

PostNL automatically provides you with the correct shipmentlabel. Track & trace and billing for all shipments are based on the S10 barcode. 

Note: You have to use the latest version of the Labelling API (2.2) or Shipping API (V1).


# Cargo

## Standard cargo products

Cargo products allow you to send pallet shipments to several European countries. PostNL Pakketten offers the following Cargo services:

* Benelux Freight: pallets with destination Belgium, The Netherlands and Luxembourg 
* Euro Freight: pallets with destination Europe, except Belgium, The Netherlands and Luxembourg. 
* Guaranteed delivery (only domestic shipments) 
* Cargo pickup 
* Half Europallets 
* Roll cage containers
* ADR-shipments

The following conditions applies:

* Pallets can only be sent to **B2B addresses**, not to Post office boxes or consumers.

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3606</p>
      </td>
      <td>
        <p>AVG Pallet Pharma&Care 2-8 C</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3607</p>
      </td>
      <td>
        <p>AVG Pallet Pharma&Care 15-25 C</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3608</p>
      </td>
      <td>
        <p>AVG Cargo Parcel Pharma&Care 2-8 C</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3609</p>
      </td>
      <td>
        <p>AVG Cargo Parcel Pharma&Care 15-25 C</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3610</p>
      </td>
      <td>
        <p>AVG Pallet NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3613</p>
      </td>
      <td>
        <p>AVG Pallet NL + ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3618</p>
      </td>
      <td>
        <p>AVG Pallet BE</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3621</p>
      </td>
      <td>
        <p>AVG Pallet BE + ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3622</p>
      </td>
      <td>
        <p>AVG Pallet LU</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3625</p>
      </td>
      <td>
        <p>AVG Pallet LU + ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3626</p>
      </td>
      <td>
        <p>AVG Euro Freight Pallet</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3627</p>
      </td>
      <td>
        <p>AVG Euro Freight Parcel Plus</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3630</p>
      </td>
      <td>
        <p>AVG Parcel Plus NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3633</p>
      </td>
      <td>
        <p>AVG Parcel Plus NL + ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3638</p>
      </td>
      <td>
        <p>AVG Parcel Plus BE</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3641</p>
      </td>
      <td>
        <p>AVG Parcel Plus NL + ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3642</p>
      </td>
      <td>
        <p>AVG Parcel Plus LU</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3645</p>
      </td>
      <td>
        <p>AVG Parcel Plus LU + ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3657</p>
      </td>
      <td>
        <p>AVG Half Europallet NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3658</p>
      </td>
      <td>
        <p>AVG Half Europallet BE</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3659</p>
      </td>
      <td>
        <p>AVG Half Europallet LU</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3696</p>
      </td>
      <td>
        <p>AVG Roll Cage container NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3697</p>
      </td>
      <td>
        <p>AVG Roll Cage container Full BE</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3698</p>
      </td>
      <td>
        <p>AVG Roll Cage container Empty NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3699</p>
      </td>
      <td>
        <p>AVG Roll Cage container Empty BE</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager.

\*\*For ADR shipments, please ask your PostNL Cargo accountmanager for the documentation.

**Country codes Eurofreight**

<table>
  <thead>
    <tr>
      <th>Destination</th>
      <th>Country code ISO2</th>
      <th>Destination</th>
      <th>Country code ISO2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Andorra</td>
      <td>AD</td>
      <td>Austria</td>
      <td>AT</td>
    </tr>
    <tr>
      <td>Bosnia-Herzegovina</td>
      <td>BA</td>
      <td>Bulgaria</td>
      <td>BG</td>
    </tr>
    <tr>
      <td>Switzerland</td>
      <td>CH</td>
      <td>Czech Republic</td>
      <td>CZ</td>
    </tr>
    <tr>
      <td>Germany</td>
      <td>DE</td>
      <td>Denmark</td>
      <td>DK</td>
    </tr>
    <tr>
      <td>Estonia</td>
      <td>EE</td>
      <td>Spain</td>
      <td>ES</td>
    </tr>
    <tr>
      <td>Finland</td>
      <td>FI</td>
      <td>France</td>
      <td>FR</td>
    </tr>
    <tr>
      <td>Croatia</td>
      <td>HR</td>
      <td>Hungary</td>
      <td>HU</td>
    </tr>
    <tr>
      <td>Italy</td>
      <td>IT</td>
      <td>Liechtenstein</td>
      <td>LI</td>
    </tr>
    <tr>
      <td>Lithuania</td>
      <td>LT</td>
      <td>Luxembourg</td>
      <td>LU</td>
    </tr>
    <tr>
      <td>Latvia</td>
      <td>LV</td>
      <td>Monaco</td>
      <td>MC</td>
    </tr>
    <tr>
      <td>Montenegro</td>
      <td>ME</td>
      <td>Norway</td>
      <td>NO</td>
    </tr>
    <tr>
      <td>Poland</td>
      <td>PL</td>
      <td>Portugal</td>
      <td>PT</td>
    </tr>
    <tr>
      <td>Romania</td>
      <td>RO</td>
      <td>Serbia</td>
      <td>RS</td>
    </tr>
    <tr>
      <td>Sweden</td>
      <td>SE</td>
      <td>Slovenia</td>
      <td>SI</td>
    </tr>
    <tr>
      <td>Slovakia</td>
      <td>SK</td>
      <td>San Marino</td>
      <td>SM</td>
    </tr>
    <tr>
      <td>Vatican City</td>
      <td>VA</td>
      <td/>
      <td/>
    </tr>
  </tbody>
</table>

**Barcode type**<br>
Cargo barcodes can be generated via the PostNL API, using the Barcode method. Details are mentioned in the Barcode method documentation. The barcode type is 3S and the barcode length is 15.

**Multiple or different items in one shipment**<br>
When having a shipment with different load carriers for the same receiver address.(Pallets in combination with a Roll Cage Container in one shipment for example), use the ‘content’ field (in Shipments -> Shipment, String [0-35]) to let us know which load carrier the item will be on. Remark: This is not a necessary field for shipping a standard pallet or parcel plus. Always consult your account manager before implementing the load carriers. The following carriers can be used for with the different product codes:

<table>
  <thead>
    <tr>
      <th>Load carrier</th>
      <th>Product code</th>
      <th>Description</th>
      <th>Country</th>
      <th>Special</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3606</p>
      </td>
      <td>
        <p>AVG Pallet Pharma&Care 2-8 C</p>
      </td>
      <td>
        <p>BENELUX</p>
      </td>
      <td>
        <p>Pharma&Care</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3607</p>
      </td>
      <td>
        <p>AVG Pallet Pharma&Care 15-25 C</p>
      </td>
      <td>
        <p>BENELUX</p>
      </td>
      <td>
        <p>Pharma&Care</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
      </td>
      <td>
        <p>3608</p>
      </td>
      <td>
        <p>AVG Cargo Parcel Pharma&Care 2-8 C</p>
      </td>
      <td>
        <p>BENELUX</p>
      </td>
      <td>
        <p>Pharma&Care</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
      </td>
      <td>
        <p>3609</p>
      </td>
      <td>
        <p>AVG Cargo Parcel Pharma&Care 15-25 C</p>
      </td>
      <td>
        <p>BENELUX</p>
      </td>
      <td>
        <p>Pharma&Care</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3610</p>
      </td>
      <td>
        <p>AVG Pallet NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3613</p>
      </td>
      <td>
        <p>AVG Pallet NL + ADR</p>
      </td>
      <td>
        <p>NL</p>
      </td>
      <td>
        <p>ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3618</p>
      </td>
      <td>
        <p>AVG Pallet BE</p>
      </td>
      <td>
        <p>BE</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3621</p>
      </td>
      <td>
        <p>AVG Pallet BE + ADR</p>
      </td>
      <td>
        <p>BE</p>
      </td>
      <td>
        <p>ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3622</p>
      </td>
      <td>
        <p>AVG Pallet LU</p>
      </td>
      <td>
        <p>LUX</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3625</p>
      </td>
      <td>
        <p>AVG Pallet LU + ADR</p>
      </td>
      <td>
        <p>LUX</p>
      </td>
      <td>
        <p>ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>BLK, EUR, EWP, KTF, P, P+, P1X, P2X, P3X</p>
      </td>
      <td>
        <p>3626</p>
      </td>
      <td>
        <p>AVG Euro Freight Pallet</p>
      </td>
      <td>
        <p>INT (NOT BENELUX)</p>
      </td>
      <td>
        <p>All combinations</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
      </td>
      <td>
        <p>3627</p>
      </td>
      <td>
        <p>AVG Euro Freight Parcel Plus</p>
      </td>
      <td>
        <p>INT (NOT BENELUX)</p>
      </td>
      <td>
        <p>All combinations</p>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
      </td>
      <td>
        <p>3630</p>
      </td>
      <td>
        <p>AVG Parcel Plus NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
        <p>&nbsp;</p>
      </td>
      <td>
        <p>3633</p>
      </td>
      <td>
        <p>AVG Parcel Plus NL + ADR</p>
      </td>
      <td>
        <p>NL</p>
      </td>
      <td>
        <p>ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
        <p>&nbsp;</p>
      </td>
      <td>
        <p>3638</p>
      </td>
      <td>
        <p>AVG Parcel Plus BE</p>
      </td>
      <td>
        <p>BE</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
        <p>&nbsp;</p>
      </td>
      <td>
        <p>3641</p>
      </td>
      <td>
        <p>AVG Parcel Plus BE + ADR</p>
      </td>
      <td>
        <p>BE</p>
      </td>
      <td>
        <p>ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
        <p>&nbsp;</p>
      </td>
      <td>
        <p>3642</p>
      </td>
      <td>
        <p>AVG Parcel Plus LU</p>
      </td>
      <td>
        <p>LUX</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>C, C+, ZAK</p>
        <p>&nbsp;</p>
      </td>
      <td>
        <p>3645</p>
      </td>
      <td>
        <p>AVG Parcel Plus LU + ADR</p>
      </td>
      <td>
        <p>LUX</p>
      </td>
      <td>
        <p>ADR</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>HEP, MP</p>
      </td>
      <td>
        <p>3657</p>
      </td>
      <td>
        <p>AVG Half Europallet NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>HEP, MP</p>
      </td>
      <td>
        <p>3658</p>
      </td>
      <td>
        <p>AVG Half Europallet BE</p>
      </td>
      <td>
        <p>BE</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>HEP, MP</p>
      </td>
      <td>
        <p>3659</p>
      </td>
      <td>
        <p>AVG Half Europallet LU</p>
      </td>
      <td>
        <p>LUX</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>RC</p>
      </td>
      <td>
        <p>3696</p>
      </td>
      <td>
        <p>AVG Roll Cage container Full NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>RC</p>
      </td>
      <td>
        <p>3697</p>
      </td>
      <td>
        <p>AVG Roll Cage container Full BE</p>
      </td>
      <td>
        <p>BE</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>RCL</p>
      </td>
      <td>
        <p>3698</p>
      </td>
      <td>
        <p>AVG Roll Cage container Empty NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>RCL</p>
      </td>
      <td>
        <p>3699</p>
      </td>
      <td>
        <p>AVG Roll Cage container Empty BE</p>
      </td>
      <td>
        <p>BE</p>
      </td>
      <td>
        <p>&nbsp;</p>
      </td>
    </tr>
  </tbody>
</table>

**Remarks for the truck driver**<br>
Do you have a specific remark for the truck driver, for example ‘Please ring at the blue gate’, use the ‘Remark’ field (in Shipments -> Shipment, String [0-255]).

## Guaranteed cargo delivery

Combine one of the above product codes with one of the following product options:

* 118;007 for delivery before 10 am
* 118;008 for delivery before 12 am
* 118;013 for delivery before 14 pm
* 118;028 for delivery between 07:00 – 08:00
* 118;017 for delivery between 08:00 – 09:00
* 118;012 for delivery between 08:00 – 17:00
* 118;029 for delivery between 09:00 – 18:00
* 118;040 for delivery between 10:00 – 18:00
* 118;030 for delivery between 12:00 – 18:00
* 118;041 for delivery between 14:00 – 18.00

\*It is mandatory to use a combination of product code and a product option.

\*\*Please note that guaranteed delivery is only allowed for shipments in the Netherlands.

## Cargo pickup

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3606 **</p>
      </td>
      <td>
        <p>AVG Pallet Pharma&Care 2-8 C</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3607 **</p>
      </td>
      <td>
        <p>AVG Pallet Pharma&Care 15-25 C</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3608 **</p>
      </td>
      <td>
        <p>AVG Cargo Parcel Pharma&Care 2-8 C</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3609 **</p>
      </td>
      <td>
        <p>AVG Cargo Parcel Pharma&Care 15-25 C</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3610 **</p>
      </td>
      <td>
        <p>AVG Pallet NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3630 **</p>
      </td>
      <td>
        <p>AVG Parcel Plus NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3657 **</p>
      </td>
      <td>
        <p>AVG Half Europallet NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3696 **</p>
      </td>
      <td>
        <p>AVG Roll Cage container NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3696**</p>
      </td>
      <td>
        <p>AVG Roll Cage container NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3618**</p>
      </td>
      <td>
        <p>AVG Pallet BE</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3638**</p>
      </td>
      <td>
        <p>AVG Cargo Parcels BE</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3658**</p>
      </td>
      <td>
        <p>AVG Half Europallet BE</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3697**</p>
      </td>
      <td>
        <p>AVG Roll Cage container BE</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3622**</p>
      </td>
      <td>
        <p>AVG Pallet LU</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3642**</p>
      </td>
      <td>
        <p>AVG Cargo Parcels LU</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3659**</p>
      </td>
      <td>
        <p>AVG Half Europallet LU</p>
      </td>
    </tr>
  </tbody>
</table>

\*These products can only be used after consulting your PostNL Pakketten account manager.

\*\*It is mandatory to use a combination of product code and a product option.

Combine these product codes with the following product option:

* product option: characteristic 135, option 001

These product codes must be combined with a pickup address (type 04)

**Business rules**

* Customer number is required.

# Returns

## Returns to a Business reply number (Antwoordnummer)

At PostNL we offer multiple return solutions. See below which solution fits the best and find out the implementation specifications.

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2285</td>
      <td>Single label</td>
    </tr>
    <tr>
      <td>2285</td>
      <td>Smart returns</td>
    </tr>
    <tr>
      <td>2285</td>
      <td>Label for electronic appliances (e-waste)</td>
    </tr>
    <tr>
      <td>- **</td>
      <td>Label in the box</td>
    </tr>
    <tr>
      <td>- **</td>
      <td>Shipping & Return label</td>
    </tr>
  </tbody>
</table>

\* These product codescan only be used after consulting your PostNL Pakketten account manager. 

\** No separate product code, create your return label at the same moment as you create the outbound shipment label.

Product should be combined with at least one or more return services.

<table>
  <thead>
    <tr>
      <th>Product option (characteristic/option)</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>152/025</td>
      <td>Smart returns</td>
    </tr>
    <tr>
      <td>152/026</td>
      <td>Shipping & Return label</td>
    </tr>
    <tr>
      <td>152/027</td>
      <td>Single label</td>
    </tr>
    <tr>
      <td>152/028</td>
      <td>Label in the box</td>
    </tr>
    <tr>
      <td>191/001</td>
      <td>Return term 35 days</td>
    </tr>
  </tbody>
</table>

The standard return term after pre-announcement is 20 days. Research has shown that most consumers return within this time frame and therefore this standard is set. An additional product option of 100 days return term is available upon request, please contact your account manager.     

__Smart Returns__

PostNL offers the possibility of printing the Return label with a business reply number return address at a PostNL location. This is convenient for the returning consumer because it is a label free solution. By adding the provided product options in the API call PostNL will provide an additional barcode in the response. The barcode is shared digitally from the webshop to the returning consumer and is scanned at handover to PostNL.

Return labels require some specific fields to be used:

* Address of receiver: Shipment/Address/AddressType 01, always a business reply number 
* Address of sender: Customer/Address/AddressType 02
* Product code: 2285
* Product option: characteristic: 152 and option: 025 and if necessary, characteristic: 191 and option: 001
* Sender contact information required: contacttype 02, with emailaddress of consumer. Consumer is sender, fill in the emailaddress to make sure consumer is informed.
* Return barcode: Shipment/Barcode

_NOTE: Digital ISO 128 barcode must be shared no earlier than 10 minutes after the API request is sent to PostNL to ensure a smooth handover process._

__Shipping & return label__

PostNL offers the possibility of returning your parcel with the same label as is used for the outbound parcel. The receivers can use this label option to return the shipments free of charge via a PostNL location or at the door when a PostNL driver comes to deliver another parcel. 

Available from Q4 (2022) upon request, please contact your account manager.

Return labels require some specific fields to be used:

* Address of receiver: Shipment/Address/AddressType 01
* Address of sender: Customer/Address/AddressType 02
* Return address: Shipment/Address/AddressType 08, always a business reply number
* Product code of outbound shipment (eg 3085)
* Product option: characteristic: 152 and option: 026 and characteristic: 191 and option: 001 
* Return barcode: Shipment/ReturnBarcode 
* Required contact information: contacttype 01, with email address of consumer. Fill in the email address to make sure consumer is informed.

__Single Label__

PostNL Parcels offers the possibility of providing a single return label that allows consumers to send parcels to yourBusinessreply number. The return label is provided from the webshop to the returning consumer and is printed and applied to the parcel by the consumer.  The consumer can use this label to return the shipments free of charge via a PostNL location or return at the door when a PostNL driver comes to deliver another parcel. 

Return labels require some specific fields to be used: 

* Address of receiver: Shipment/Address/AddressType 01. Always a business reply number 
* Address of sender: Customer/Address/AddressType 02 
* Product code: 2285 
* Product option: characteristic: 152 and option: 027 and if necessary, characteristic: 191 and option: 001 
* Sender contact information required: contacttype 02, with emailaddress of consumer. Consumer is sender, fill in the emailaddress to make sure consumer is informed.
* Return barcode: Shipment/Barcode

__Label in the box__

PostNL offers the possibility of sending return labels along with parcels. We call this the ‘Label in the box return label’. The receivers can usethis label to return the shipments free of charge via a PostNL location or return at the door when a PostNL driver comes to deliver another parcel. 

The barcode of the return label is linked to the barcode of the outbound shipment label.

Return labels require some specific fields to be used:

* Address of receiver: Shipment/Address/AddressType 01
* Address of sender: Customer/Address/AddressType 02 
* Return address: Shipment/Address/AddressType 08, always a business reply number 
* Product code of outbound shipment (for example: 3085) 
* Product option: characteristic: 152 and option: 028 and characteristic: 191 and option: 001 
* Return barcode: Shipment/ReturnBarcode 
* Required contact information: contacttype 01, with emailaddress of consumer. Fill in the emailaddress to make sure consumer is informed.

__Returns to an e-waste Business reply number (Antwoordnummer)__

PostNL offers the possibility to create a personalized Businessreply number that is connected to our recycling partner for e-waste. Our partner will process the e-waste returned by the consumer. The same implementation is applied here as to business reply numbers in general. The e-waste business reply number is only available in combination with single label and smart returns.  

*Single label*

PostNL Parcels offers the possibility of providing a single return label that allows consumers to send parcels to yourBusinessreply number. The return label is provided from the webshop to the consumer  and should be printed by the consumer.   The consumer can use this label to return the shipments free of charge via a PostNL location or at the door when a PostNL driver comes to deliver another parcel. 

Return labels require some specific fields to be used:

* Address of receiver: Shipment/Address/AddressType 01. Always a business reply number 
* Address of sender: Customer/Address/AddressType 02 
* Product code: 2285 
* Product option: characteristic: 152 and option: 027 and if necessary, characteristic: 191 and option: 001 
* Sender contact information required: contacttype 02, with email address of consumer. Consumer is sender, fill in the email address to make sure consumer is informed.
* Return barcode: Shipment/Barcode

*Smart Returns*

PostNL offers the possibility of printing the Return label with a business reply number return address at a PostNL location. This is convenient for the returning customer because it is a label free solution. By adding the provided product options in the API call PostNL will provide an additional barcode in the response. The barcode is shared digitally from the webshop to the returning customer and is scanned at handover to PostNL.

Return labels require some specific fields to be used:

* Address of receiver: Shipment/Address/AddressType 01, always a business reply number 
* Address of sender: Customer/Address/AddressType 02 
* Product code: 2285 
* Product option: characteristic: 152 and option: 025 and if necessary, characteristic: 191 and option: 001 
* Sender contact information required: contacttype 02, with emailaddress of consumer. Consumer is sender, fill in the email address to make sure consumer is informed.  
* Return barcode: Shipment/Barcode

_NOTE: Digital ISO 128 barcode must be shared no earlier than 10 minutes after the API request is sent to PostNL to ensure a smooth handover process._

## Returns to a home address

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3285</td>
      <td>Single return label to home address</td>
    </tr>
    <tr>
      <td>3285</td>
      <td>Smart return label to home address</td>
    </tr>
    <tr>
      <td>- **</td>
      <td>Label in the box</td>
    </tr>
    <tr>
      <td>- **</td>
      <td>Shipping & Return label</td>
    </tr>
  </tbody>
</table>

\* These product codescan only be used after consulting your PostNL Pakketten account manager.

\** No separate product code, create your return label at the same moment as you create the outbound shipment label.

*Services*

Product should be combined with at least one or more return services (product options):

<table>
  <thead>
    <tr>
      <th>Product option (characteristic/option)</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>152/025</td>
      <td>Smart returns</td>
    </tr>
    <tr>
      <td>152/026</td>
      <td>Shipping & Return label</td>
    </tr>
    <tr>
      <td>152/027</td>
      <td>Single label</td>
    </tr>
    <tr>
      <td>152/028</td>
      <td>Label in the box</td>
    </tr>
    <tr>
      <td>191/001</td>
      <td>Return term 35 days</td>
    </tr>
  </tbody>
</table>

The standard return term after pre-announcement is 20 days. Research has shown that most consumers return within this time frame and therefore this standard is set. An additional product option of 100 days return term is available upon request, please contact your account manager.

**Smart Returns**

PostNL offers the possibility of printing the Return label with a home address for returns at a PostNL location. This is convenient for the returning customer because it is a label free solution.  By adding the provided product options (see below) in the API call , PostNL will provide an additional barcode in the response.  The barcode is shared digitally from the webshop to the returning customer and is scanned at handover to PostNL. 

Return labels require some specific fields to be used: 

* Address of receiver: Shipment/Address/AddressType 01. Always a home address 
* Address of sender: Customer/Address/AddressType 02 
* Product code: 3285 
* Product option: characteristic: 152 and option: 025 and if necessary, characteristic: 191 and option: 001
* Sender contact information required: contacttype 02, with emailaddress of consumer. Consumer is sender, fill in the emailaddress to make sure consumer is informed.
* Return barcode: Shipment/Barcode

_NOTE: Digital ISO 128 barcode must be shared no earlier than 10 minutes after the API request is sent to PostNL to ensure a smooth handover process._

**Shipping & Return label**

PostNL offers the possibility of returning your parcel with the same label as is used for the outbound parcel. The receivers can use this label option to return the shipments free of charge via a PostNL location or at the door when a PostNL driver comes to deliver another parcel. 

Available from Q4 (2022) upon request, please contact your account manager.

Return labels require some specific fields to be used:

* Address of receiver: Shipment/Address/AddressType 01
* Address of sender: Customer/Address/AddressType 02
* Return address: Shipment/Address/AddressType 08, always a home address 
* Product code of outbound shipment (eg 3085) 
* Product option: characteristic: 152 and option: 026 and characteristic: 191 and option: 001 
* Return barcode: Shipment/ReturnBarcode 
* Required contact information: contacttype 01, with emailaddress of consumer. Fill in the emailaddress to make sure consumer is informed. 

**Single Label**

PostNL Parcels  offers the possibility of providing a single return label, that allows customers to send parcels to a home address for returns. The return label is provided from the webshop to the consumer and should be printed by the consumer. The consumer can use this label to return the shipments free of charge via a PostNL location or at the door when a PostNL driver comes to deliver another parcel. 

Return labels require some specific fields to be used: 

* Address of receiver: Shipment/Address/AddressType 01. Always a home address 
* Address of sender: Customer/Address/AddressType 02
* Product code: 3285 
* Product option: characteristic: 152 and option: 027 and if necessary, characteristic: 191 and option: 001 
* Sender contact information required: contacttype 02, with emailaddress of consumer. Consumer is sender, fill in the emailaddress to make sure consumer is informed.  
* Return barcode: Shipment/Barcode

**Label in the Box**

PostNL offers the possibility of sending return labels along with parcels. We call this the ‘Label in the box return label’. The receivers can usethis labelto return the shipments free of charge via a PostNL location or at the door when a PostNL driver comes to deliver another parcel. 

The barcode of the return label is linked to the barcode of the outbound shipment label.

Return labels require some specific fields to be used:

* Address of receiver: Shipment/Address/AddressType 01 
* Address of sender: Customer/Address/AddressType 02 
* Return address: Shipment/Address/AddressType 08, always a home address  
* Product code of outbound shipment (eg 3085) 
* Product option: characteristic: 152 and option: 028 and characteristic: 191 and option: 001  
* Return barcode: Shipment/ReturnBarcode 
* Required contact information: contacttype 01, with emailaddress of consumer. Fill in the emailaddress to make sure consumer is informed.

## Digital notification

Consumers prefer to receive a digital notification instead of paper notifications. By providing the e-mail address of the consumer in the pre-announcement PostNL can share real-time information of the return parcel status. By implementing this, consumers will receive a digital notification and can easily track their return parcel in the PostNL app causing less customer calls.  

Implementation: 

**Shipping & return label, Label in the Box**

* Contacttype is 01. The consumer starts as the receiver of the outbound parcel. During the return journey PostNL will make sure that the contact information of the consumer is placed correctly. The consumer  can now also follow its parcel as a return parcel in track & trace and will receive digital proof of handover. 

Step 1 – fill in contact type ‘01’<br>
Step 2 – enter the e-mail address of the consumer at  ‘receiver@gmail.com’<br>
Step 3 – Enter telephone number of the consumer (optional)

**Smart returns, single label**

Implementation:

* Contact type is 02. The consumer is now the sender of the parcel. The consumer will receive digital  proof of handover and can follow its return parcel in Track & Trace.

Step 1 – fill in contact type ‘02’<br>
Step 2 – enter the e-mail address of the consumer at  ‘receiver@gmail.com’<br>
Step 3 – Enter telephone number of the consumer (optional)

# Extra @ Home

## Standard Extra @ Home products

PostNL Extra@Home has introduced a unique service whereby large and heavy goods, also named XL goods, will be delivered and installed. These XL goods are furniture, televisions, refrigerators and washing machines.

Before the delivery takes place, customers will receive a text message or e-mail informing them of the delivery window (timeframe). On the day of delivery, the customers will receive a second notification with the exact time of delivery. Extra@Home knows 2 kinds of delivery: by one-man or two-men transport, depending on the dimensions of the order.

Specifications of the dimension criteria of Extra@Home products can be requested at [eh-logistiek@postnl.nl](mailto:eh-logistiek@postnl.nl). Products should only be addressed to private home addresses, so not to P.O boxes or pickup points.

Delivery will be on weekdays (Monday till Friday) between 08:00 and 21:00 and optional on Saturday (with a surcharge).

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
      <th>Available destinations</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3628</p>
      </td>
      <td>
        <p>Extra@Home Top service 2 person delivery NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3629</p>
      </td>
      <td>
        <p>Extra@Home Top service Btl 2 person delivery</p>
      </td>
      <td>
        <p>BE;LU</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3653</p>
      </td>
      <td>
        <p>Extra@Home Top service 1 person delivery NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3783</p>
      </td>
      <td>
        <p>Extra@Home Top service&nbsp;Btl 1 person delivery</p>
      </td>
      <td>
        <p>BE;LU</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3790</p>
      </td>
      <td>
        <p>Extra@Home Drempelservice 1 person delivery NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3791</p>
      </td>
      <td>
        <p>Extra@Home Drempelservice 2 person delivery NL</p>
      </td>
      <td>
        <p>NL</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3792</p>
      </td>
      <td>
        <p>Extra@Home Drempelservice Btl 1 person delivery</p>
      </td>
      <td>
        <p>BE; LU</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3793</p>
      </td>
      <td>
        <p>Extra@Home Drempelservice Btl 2 persons delivery</p>
      </td>
      <td>
        <p>BE; LU</p>
      </td>
    </tr>
  </tbody>
</table>

NL: Netherlands, BE: Belgium, LU: Luxembourg<br>
\*These articles can only be used after consulting your PostNL Pakketten accountmanager.

Please always choose directly the correct product code for the order to prevent delivery problems.

Combine these product codes with the following product option if you want to send with COD:

* product option: chararteristic 003 option 003

**Business rules**

* Shipment.Content is required 
* Shipment.Reference is required (this should be unique for each shipment as this will be used to generate the Extra@Home order reference) 
* Volume is required (approximation suffices) 
* Weight is required (approximation suffices) 
* Mobile phone number required for text messages with ETA; 
* E-mail adress required for link Customer Portal incl. Track &Trace.

## Extra @ Home pickup service

The pickup service allows you to instruct a PostNL Parcels driver to go to a specific address on a specific date to retrieve (a) parcel(s). The parcel(s) will then be delivered to an address specified by you. The driver will provide the shipment label, so there is no option to create one via the API. For these products, the Confirming WebService must be used. For an example of a Extra @ Home Pickup shipment, please refer to the Confirming WebService documentation.

<table>
  <thead>
    <tr>
      <th>Product code *</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>3794</p>
      </td>
      <td>
        <p>Extra @ Home Doorstep Service&nbsp;1 man Pick Up</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3795</p>
      </td>
      <td>
        <p>Extra @ Home Doorstep Service 2 men Pick Up</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3781</p>
      </td>
      <td>
        <p>Extra @ Home Topservice 1 man Pick Up</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3780</p>
      </td>
      <td>
        <p>Extra @ Home Topservice 2 men Pick Up</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3796</p>
      </td>
      <td>
        <p>Extra @ Home Doorstep Service 1 man foreign Pick Up</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3797</p>
      </td>
      <td>
        <p>Extra @ Home Doorstep Service 2 men foreign Pick Up</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3784</p>
      </td>
      <td>
        <p>Extra @ Home Topservice 1 man foreign Pick Up</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>3782</p>
      </td>
      <td>
        <p>Extra @ Home Topservice 2 men foreign Pick Up</p>
      </td>
    </tr>
  </tbody>
</table>

\*These articles can only be used after consulting your PostNL Pakketten accountmanager.

**Address type for pick-up**<br>
PostNL internal applications validate the receiver address. In case the spelling of addresses should be different according to our PostNL information, the address details will be corrected. This can be noticed in Track & Trace. Please note that the webservice will not add address details. Street and City fields will only be printed when they are in the call towards the labeling webservice.

The element Address type is a code in the request. Possible values for pickup orders:

<table>
  <thead>
    <tr>
      <th>Code</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>02</p>
      </td>
      <td>
        <p>Sender</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>03</p>
      </td>
      <td>
        <p>Alternative sender address</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>04</p>
      </td>
      <td>
        <p>Collection address</p>
      </td>
    </tr>
  </tbody>
</table>