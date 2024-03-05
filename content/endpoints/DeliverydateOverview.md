# Deliverydate API

### Summary
    
* Calculate expected delivery date based on shipping date or required shipping date based on requested delivery date.
* Input: Address, postalcode, shipping- or delivery date and delivery options.
* Output: Delivery date and Sent date.

Please note that you can use the all-in-one [Checkout API](#tag/Checkout) as well. This API combines he the functionality of the DeliveryDate, Location and Timeframe webservices. So it will be easier to implement the PostNL delivery options and there is less overhead in requesting the PostNL services by using this 3-in-1 API.

### Guidelines

At the <a href="https://developer.postnl.nl/" target="_blank" rel="noopener noreferrer">Developer Portal</a> you can find information about the use and functionality of the API. It is strongly recommended that you read this carefully before starting the implementation.

<button type="button">
  <a href="https://developer.postnl.nl/browse-apis/delivery-options/deliverydate-webservice/" target="_blank" rel="noopener noreferrer">Documentation</a>
</button>

### Versioning

<table>
  <tbody>
    <tr>
      <th>API</th>
      <th>Release date</th>
      <th>Status</th>
      <th>Release notes</th>
      <th>Schema changes</th>
      <th>Available as</th>
    </tr>
    <tr>
      <td>v1_0</td>
      <td>Oct 07, 2013</td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>v1_1</td>
      <td>Jan 24, 2014</td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>v1_2</td>
      <td>Aug 14, 2014</td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>v2_0</td>
      <td>Aug 14, 2015</td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>v2_1</td>
      <td>Nov 03, 2015</td>
      <td>Supported</td>
      <td>See below</td>
      <td>Yes</td>
      <td>SOAP</td>
    </tr>
    <tr>
      <td>v2_2</td>
      <td>Aug 24, 2017</td>
      <td>Current version</td>
      <td>See below</td>
      <td>Yes</td>
      <td>REST and SOAP</td>
    </tr>
  </tbody>
</table>

### Release notes

#### v2.0

*   CutOffTime and CutOffTimeForSundaySorting replaced by CutOffTimes list. In the previous version of the GetDeliveryDate method, cut off times were specified for weekdays and Sunday in two fields. It is now possible to specify cut off times for every day of the week in the new CutOffTimes field.*   Options field added. It is now possible to specify which delivery options should be considered when returning a delivery or sent date using the new Options field.*   New and updated address fields. Several address fields have been added to the GetDeliveryDate and GetSendDate elements to specify the delivery address more precisely. These fields are: Street, HouseNrExt, City and CountryCode.  
    Furthermore, the HouseNumber field has been renamed to HouseNr.

#### v2.1

*   GetDeliveryDateResponse.Option is removed from the interface. The GetDeliveryDateResponse.Options is added to the interface.

#### v2.2

*   Thee following fields have been added to the interface:  
    OriginCountryCode  
    CutoffTime.Available  
    New delivery option: MyTime (Delivery on demand)
    
    __NOTE: THIS PRODUCT NO LONGER EXIST__

* If applicable, sustainability scores are now returned for each option