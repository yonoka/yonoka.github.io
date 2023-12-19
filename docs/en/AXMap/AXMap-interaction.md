# Map Interaction

## `setAreaMap(areaId) -> {void}`

Set area map

### Parameters

| Name | Data Type | Description |
| -------- | -------- | ------------ |
| `areaId` | string | Map area ID |

### Return Value

none

### Example

```javascript
...
axMap.setAreaMap("<areaId>");
...
````

## `setMapCenter(coordinates) -> {void}`

Set the map center point

### Parameters

| Name | Data Type | Description |
| ------------- | ------------- | ----------------- |
| `coordinates` | array<number> | center point coordinates [x, y] |

### Return Value

none

### Example

```javascript
...
axMap.setMapCenter([0, 0]);
...
````

## `zoomTo(zoom) -> {void}`

Set the map zoom level

### Parameters

| Name | Data Type | Description |
| ------ | -------- | ----------------------------- |
| `zoom` | number | The zoom level of the map, the value range is 0~22 |

### Return Value

none

### Example

```javascript
...
axMap.zoomTo(10);
...
````

## `fly(coordinates) -> {void}`

map fly to a point

### Parameters

| Name | Data Type | Description |
| ------------- | ------------- | ----------------- |
| `coordinates` | array<number> | target point coordinates [x, y] |

### Return Value

none

### Example

```javascript
...
axMap.fly([0, 0]);
...
````

## `getCurrentPointPosition(featureId) -> {object}`

Get the currently selected point pose

### Parameters

| Name | Data Type | Description |
| ----------- | -------- | ------ |
| `featureId` | string | point identifier |

### Return Value `object`

pose information

* `x` - coordinate x component
* `y` - the y component of the coordinate
* `yaw` - heading angle

### Example

```javascript
...
const pose = axMap.getCurrentPointPosition("<featureId>");

console.log(pose); // {x:1, y: 2, yaw: 3}
...
````

## `getFeature(id) -> {object}`

Get feature information by ID

### Parameters

| Name | Data Type | Description |
| ---- | -------- | ------------ |
| `id` | string | feature identifier |

### Return Value `object`

feature information; structure reference [https://geojson.org/](https://geojson.org/)

### Example

```javascript
...
const feature = axMap.getFeature("<featureId>");
...
````

## `getPlaceList() -> {any}`

Get all location points

### Parameters

none

### Return Value `any`

List of location points; structure reference [https://geojson.org/](https://geojson.org/)

### Example

```javascript
...
const list = axMap.getPlaceList();
...
````

## `setClickMapCallback(callback) -> {void}`

Set the click map callback method

### Parameters

| Name | Data Type | Description |
| ---------- | -------- | -------- |
| `callback` | function | callback method |

### Return Value

none

### Example

```javascript
...
axMap.setClickMapCallback(val => {
  console.log(val.type); // fixed to 'LayerPoint'
  console.log(val.data); // Clicked element, data structure reference GeoJSON
});
...
````

## `setSelectedFeatures(featureId) -> {void}`

Select the feature in the map based on the ID

### Parameters

| Name | Data Type | Description |
| ------------- | -------- | ----------------------------------------- |
| `featureId` | string | feature ID, multiple feature IDs are separated by commas |

### Return Value

none

### Example

```javascript
...
axMap.setSelectedFeatures("<featureId>");
...
````
