# Timeframes API

### Summary
    
* Reason to Call: To get a timeframe in which a parcel is estimated to be delivered.
* Input: Details of dates, delivery options and the address of the recipient.
* Output: Expected delivery timeframes and the possible reason no timeframe could be given.

Please note that you can use the all-in-one [Checkout API](#tag/Checkout) as well. This API combines he the functionality of the DeliveryDate, Location and Timeframe webservices. So it will be easier to implement the PostNL delivery options and there is less overhead in requesting the PostNL services by using this 3-in-1 API.

### Guidelines

At the <a href="https://developer.postnl.nl/" target="_blank" rel="noopener noreferrer">Developer Portal</a> you can find information about the use and functionality of the API. It is strongly recommended that you read this carefully before starting the implementation.

<button type="button">
  <a href="https://developer.postnl.nl/browse-apis/delivery-options/timeframe-webservice/" target="_blank" rel="noopener noreferrer">Documentation</a>
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
      <td>Aug 14, 2014</td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>v1_2</td>
      <td>Oct 08, 2014</td>
      <td>Not supported</td>
      <td/>
      <td/>
      <td/>
    </tr>
    <tr>
      <td>v2_0</td>
      <td>Aug 14, 2015</td>
      <td>Supported</td>
      <td>See below</td>
      <td>Yes</td>
      <td>SOAP</td>
    </tr>
    <tr>
      <td>v2_1</td>
      <td>Jun 01, 2017</td>
      <td>Current version</td>
      <td>See below</td>
      <td>Yes</td>
      <td>REST</td>
    </tr>
  </tbody>
</table>

### Release notes

#### v1.2

*   The following field has been added to the interface: Timeframe.SundaySorting*   Methods and TijdvakType replaced by options. The methods GetDeliveryTimeframes, GetDaytimeTimeframes, GetEveningTimeframes and GetMorningTimeframes have been replaced by a single GetTimeframes method. To specify the delivery option(s) for which timeframes should be returned, the field Options has been added to the Timeframe element.

#### v2.0

*   The new options Sunday and Sameday are also available in the new GetTimeframes method. The field TijdvakType which indicated which delivery option was applicable to the returned Timeframe and ReasonNoTimeframe elements has been replaced by an Options field. This field uses the same values as the new Options field in the request.*   New and updated address fields. Several address fields have been added to the Timeframe element to specify the delivery address more precisely. These fields are: Street, HouseNrExt, City and CountryCode. CountryCode is a mandatory field. For an address in the Netherlands, specify NL for this field. Furthermore, the HouseNumber field has been renamed to HouseNr.

#### v2.1

*   Added Option value ‘MyTime’ for delivery on demand.*   The following optional fields have been added to the interface (for the delivery on demand product):  
    Timeframe.Interval (used to filter certain timeframes which can be returned for delivery on demand)  
    Timeframe.TimeframeRange.Start (used to specify a specific range of timeframes to be returned for delivery on demand)  
    Timeframe.TimeframeRange.End
            
    __NOTE: THIS PRODUCT NO LONGER EXIST__
    
#### v2.2

* The following fields have been added to the interface:  
  * OriginCountryCode  
  * CutoffTime.Available
* If applicable, sustainability scores are now returned for each option