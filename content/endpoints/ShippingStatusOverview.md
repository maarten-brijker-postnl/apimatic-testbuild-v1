# Track & Trace API

### Summary
    
* Reason to Call: Receive status information about the shipments.
* Input: Customer number, barcode or reference.
* Output: Status information about the shipment(s).

Please note that we have a (pilot) webhooks solution. You can sign up for this solution by sending an email to [DEVELOPER](mailto:developer@postnl.nl). After approval and verifying a number of data our engineers will arrange this webhooks configuration.

### Guidelines

At the <a href="https://developer.postnl.nl/" target="_blank" rel="noopener noreferrer">Developer Portal</a> you can find information about the use and functionality of the API. It is strongly recommended that you read this carefully before starting the implementation.

<button type="button">
  <a href="https://developer.postnl.nl/browse-apis/send-and-track/shippingstatus-webservice/" target="_blank" rel="noopener noreferrer">Documentation</a>
</button>

### Versioning

<table>
  <tbody>
    <tr>
      <td>API </td>
      <td>Release date </td>
      <td>Status </td>
      <td>Release notes </td>
      <td>Schema Changes </td>
      <td>Available as </td>
    </tr>
    <tr>
      <td>1_1 </td>
      <td>Oct 1, 2012 </td>
      <td>Not supported </td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_2 </td>
      <td>Nov 8, 2013 </td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_3 </td>
      <td>Feb 27, 2014 </td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_4 </td>
      <td>Aug 14, 2014 </td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_5 </td>
      <td>Jan 12, 2015 </td>
      <td>Not supported </td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>1_6 </td>
      <td>Jun 01, 2017 </td>
      <td>Supported </td>
      <td>See below </td>
      <td>Yes </td>
      <td>REST and SOAP </td>
    </tr>
    <tr>
      <td>v2 </td>
      <td>Feb 12, 2018 </td>
      <td>Supported </td>
      <td>See below </td>
      <td>Yes </td>
      <td>REST </td>
    </tr>
  </tbody>
</table>

### Release notes

#### v1.3

* Changed fields in CurrentStatus response:
    Added Shipments/ProductOptions
* Changed fields in CompleteStatus response:  
    Added Shipments/ProductOptions

#### v1.6

* The following fields have been added to the interface:  
    CurrentStatusResponseShipment/DeliveryDate  
    CurrentStatusResponseShipment/Expectation  
    CompleteStatusResponseShipment/DeliveryDate  
    CompleteStatusResponseShipment/Expectation  

#### V2

* A new method has ben added to the interface;  
    /v2/status/{customernumber}/updatedshipments. This method returns the updated statuses for a particular customer number.  
    The following fields have been added to the interface;  
    * maxDays
    * language