# Route 53 Record Set GeoLocation Property<a name="aws-properties-route53-recordset-geolocation"></a>

The `GeoLocation` property is part of the [AWS::Route53::RecordSet](aws-properties-route53-recordset.md) resource that describes how Route 53 responds to DNS queries based on the geographic location of the query\. This property is not compatible with the `Region` property\.

## Syntax<a name="w13ab1c21c10d201c22c21b5"></a>

### JSON<a name="aws-properties-route53-recordset-geolocation-syntax.json"></a>

```
{
  "[ContinentCode](#cfn-route53-recordset-geolocation-continentcode)" : String,
  "[CountryCode](#cfn-route53-recordset-geolocation-countrycode)" : String,
  "[SubdivisionCode](#cfn-route53-recordset-geolocation-subdivisioncode)" : String
}
```

### YAML<a name="aws-properties-route53-recordset-geolocation-syntax.yaml"></a>

```
[ContinentCode](#cfn-route53-recordset-geolocation-continentcode): String
[CountryCode](#cfn-route53-recordset-geolocation-countrycode): String
[SubdivisionCode](#cfn-route53-recordset-geolocation-subdivisioncode): String
```

## Properties<a name="w13ab1c21c10d201c22c21b7"></a>

`ContinentCode`  <a name="cfn-route53-recordset-geolocation-continentcode"></a>
All DNS queries from the continent that you specified are routed to this resource record set\. If you specify this property, omit the `CountryCode` and `SubdivisionCode` properties\.  
For valid values, see [GeoLocation](https://docs.aws.amazon.com/Route53/latest/APIReference/API_GeoLocation.html) in the *Amazon Route 53 API Reference*\.  
*Type*: String  
*Required*: Conditional\. You must specify this or the `CountryCode` property\.

`CountryCode`  <a name="cfn-route53-recordset-geolocation-countrycode"></a>
All DNS queries from the country that you specified are routed to this resource record set\. If you specify this property, omit the `ContinentCode` property\. To specify the default location, use \* for this property\.  
For valid values, see [GeoLocation](https://docs.aws.amazon.com/Route53/latest/APIReference/API_GeoLocation.html) in the *Amazon Route 53 API Reference*\.  
*Type*: String  
*Required*: Conditional\. You must specify this or the `ContinentCode` property\.

`SubdivisionCode`  <a name="cfn-route53-recordset-geolocation-subdivisioncode"></a>
If you specified `US` for the country code, you can specify a state in the United States\. All DNS queries from the state that you specified are routed to this resource record set\. If you specify this property, you must specify `US` for the `CountryCode` and omit the `ContinentCode` property\.  
For valid values, see [GeoLocation](https://docs.aws.amazon.com/Route53/latest/APIReference/API_GeoLocation.html) in the *Amazon Route 53 API Reference*\.  
*Type*: String  
*Required*: No