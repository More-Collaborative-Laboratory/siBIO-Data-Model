# Organization

Describes the organization entity
-  `id`: Organization Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `legalName`: Organization's legal name
   -  Attribute type: **Property**. [legalName](https://schema.org/legalName)
   -  Required
-  `taxId`: The organization's tax number
   -  Attribute type: **Property**. [taxID](https://schema.org/taxID)
   -  Required
-  `ssnId`: The organization's social security number
   -  Attribute type: **Property**. 
   -  Required
-  `caeId`: The organization's economic activity code
   -  Attribute type: **Property**. 
   -  Optional
-  `address`: The company's headquarters address
   -  Attribute type: **Property**. [address](https://schema.org/address)
   -  Optional
-  `email`: Contact email address
   -  Attribute type: **Property**. [email](https://schema.org/email)
   -  Required
-  `telephone`: Mobile or telephone contact
   -  Attribute type: **Property**. [telephone](https://schema.org/telephone)
   -  Optional
-  `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon
   -  Attribute type: **GeoProperty**. 
   -  Optional



# Process

Describes a given process within a company
-  `id`: Process identifier
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Process designation
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Optional
-  `details`: Process details/characteristics
   -  Attribute type: **Property**. [text](https://schema.org/text)
   -  Optional
-  `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon
   -  Attribute type: **GeoProperty**. 
   -  Optional
-  `executedAt`: Identification of the Organization where the process is being executed.
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional



# Asset

Describes an asset within a process
-  `id`: Asset Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Asset designation
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Required
-  `category`: Asset category
   -  Attribute type: **Property**. 
   -  Optional
-  `details`: Asset description
   -  Attribute type: **Property**. [text](https://schema.org/text)
   -  Optional
-  `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon
   -  Attribute type: **GeoProperty**. 
   -  Optional
-  `usedIn`: Identification of the Process where the Asset in being used in.
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional



# MeasurementNode

Describes a given node within an asset
-  `id`: Measurement node identifier
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Process designation
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Optional
-  `details`: Process details/characteristics
   -  Attribute type: **Property**. [text](https://schema.org/text)
   -  Optional
-  `dataCategory`: Define node data reading category * `Automatic` - Measures delivered automatically by an IoT device * `Manual` - Measures introduced by a human operator * `Both` - This node have measures that are introduced by an IoT device and a human. One of : `Automatic`, `Manual`, `Both`.
   -  Attribute type: **Property**. [category](https://schema.org/category)
   -  Optional
-  `operatedBy`: Identification of the Worker currently operating the Measurement Node.
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional
-  `deployedAt`: Identification of the Asset in which the Measurement Node is deployed.
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional
-  `software`: Describes the device's software layer.
   -  Attribute type: **Property**. 
   -  Optional
-  `firmware`: Firmware version.
   -  Attribute type: **Property**. 
   -  Optional
-  `cpu`: Describes the CPU installed on the device
   -  Attribute type: **Property**. 
   -  Optional
-  `gnss`: Indicates the existence or absence of a GNSS receiver (GPS) installed or acessible by the device.
   -  Attribute type: **Property**. 
   -  Optional
-  `rfid`: Indicates the existence or absence of an RFID identification tag.
   -  Attribute type: **Property**. 
   -  Optional
-  `connectivity`: Data communication capability of the device.
   -  Attribute type: **Property**. 
   -  Optional
-  `rssi`: Indicates the value of the RSSI (in dBm) of available wireless transceivers.
   -  Attribute type: **Property**. 
   -  Optional
-  `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon
   -  Attribute type: **GeoProperty**. 
   -  Optional



# Worker

Identifies a worker within an organization
-  `id`: Worker Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `givenName`: Worker first name
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Required
-  `familyName`: Worker last name
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `taxId`: Worker Tax ID
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `ssnId`: Worker Social Security Number ID
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `functionPerformed`: The tasks and functions performed by the worker
   -  Attribute type: **Property**. 
   -  Optional
-  `worksAt`: Identification of the Organization where the Worker is currently employed.
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional



# Sensor

Sensor's description and physical variables
-  `id`: Sensor identifier
   -  Attribute type: **Property**. 
   -  Required
-  `measurementVariable`: Defines the variable that the sensor can measure * `Water` - Water consumption measurement * `Energy` - Energy consumption measurement. One of : `Water`, `Energy`.
   -  Attribute type: **Property**. 
   -  Optional
-  `measurementValue`: Measured variable quantity consumed by a given asset, within a process
   -  Attribute type: **Property**. 
   -  Optional
-  `belongsTo`: Identification of the Measurement node the sensor is connected to.
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional



## Examples

### OK


