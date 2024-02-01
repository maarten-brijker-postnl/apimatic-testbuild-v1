# Shipment API

### Summary
    
* Reason to Call: Create a barcode, shipment and send a confirmation to PostNL
* Input: All information about the shipment
* Output: One or more shipping labels

### Guidelines

At the <a href="https://developer.postnl.nl/" target="_blank" rel="noopener noreferrer">Developer Portal</a> you can find information about the use and functionality of the API. It is strongly recommended that you read this carefully before starting the implementation.

<button type="button">
  <a href="https://developer.postnl.nl/browse-apis/send-and-track/shipping-webservice/" target="_blank" rel="noopener noreferrer">Documentation</a>
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
      <td>v1</td>
      <td>April 28, 2020</td>
      <td>Current version</td>
      <td>See below</td>
      <td>-</td>
      <td>REST</td>
    </tr>
  </tbody>
</table>

### Release notes

#### v1

In comparison to the Labelling API 2.2:

* If no barcode is included in the request, a unique barcode will be generated.
* Productcode 4910 (Easy Return Service) can be used in the ProductCodeDelivery attribute. So a cross-border return shipment can be made.