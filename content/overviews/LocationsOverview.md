# Locations API

### Summary
    
* Reason to Call: Retrieve a list of pick up points that support the option for direct delivery to a standard pick up point.
* Input: Address, city and country code of the preferred location Or longitude and latitude.
* Output: Locations nearest to the supplied address, location within the supplied area or location information of the location code.

Please note that you can use the all-in-one [Checkout API](#tag/Checkout) as well. This API combines he the functionality of the DeliveryDate, Location and Timeframe webservices. So it will be easier to implement the PostNL delivery options and there is less overhead in requesting the PostNL services by using this 3-in-1 API.

### Guidelines

At the <a href="https://developer.postnl.nl/" target="_blank" rel="noopener noreferrer">Developer Portal</a> you can find information about the use and functionality of the API. It is strongly recommended that you read this carefully before starting the implementation.

<button type="button">
  <a href="https://developer.postnl.nl/browse-apis/delivery-options/location-webservice/" target="_blank" rel="noopener noreferrer">Documentation</a>
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
      <td>Jul 22, 2013</td>
      <td>Not supported</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
    </tr>
    <tr>
      <td>v1_1</td>
      <td>Aug 21, 2014</td>
      <td>Supported</td>
      <td>See below</td>
      <td>Yes</td>
      <td>SOAP</td>
    </tr>
    <tr>
      <td>v2_0</td>
      <td>Aug 14, 2015</td>
      <td>Not supported</td>
      <td>-</td>
      <td>-</td>
      <td>-</td>
    </tr>
    <tr>
      <td>v2_1</td>
      <td>May 10, 2016</td>
      <td>Supported</td>
      <td>See below</td>
      <td>Yes</td>
      <td>REST and SOAP</td>
    </tr>
  </tbody>
</table>

### Release notes

#### v1.1

* The operation GetNearestLocations has been updated with new request properties:  
  * Countrycode [M] has been added for international locations  
  * Location.City [O] has been added for better international matching  
  * Location.HouseNr [O] has been added for better international matching  
  * Location.HouseNrExt [O] has been added for better international matching  
  * Location.Street [O] has been added for better international matching
* The operation GetLocationsInArea has been updated with new request properties:  
  * Countrycode [M] has been added for international locations
  * The operation GetBLSLocation has been removed
  * The operation GetLocation has been added
  * The Location Type has been extended with international address properties.
    
#### v2.1

* The Location Type has been extended with PartnerLocationCodes (ResponseLocationCode).
* If applicable, sustainability scores are now returned for each option