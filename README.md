# jsonToDartModel

online tool for convert json to dart code

click [http://www.eyrefree.org/jsonToDartModel/](http://www.eyrefree.org/jsonToDartModel/)

## Feature
- online use, without plugin
- surport multidimensional list
- surport complex json
- surport convert all props to String type
- empty props warning
- single file
- dart keyword protected
- instant convert

## FYI
- object should have at least one property
- only first object in array will be parsed, empty array will cause error
- when select `Force String Type` , the `bool` type will not convert

## Usage
1. input json string in left textinput
2. input root class name in left bottom textinput
3. copy code by button or mouse

## Example
json string may looks like
``` json
{
  "some_snake_case_prop": "",
  "anInt": 1,
  "aDouble": 2.3,
  "aString": "hello",
  "aBool": false,
  "anObj": {
    "name": "x",
    "age": 18.1
  },
  "anObjList": [
    {
      "name": "y"
    }
  ],
  "aStrList": [
    "something"
  ],
  "multidimensional": [
    [
      [
        {
          "name": "y"
        }
      ]
    ]
  ]
}
```
named it `SomeRootEntity` and convert to dart
``` dart
  var obj = SomeRootEntity.fromJson(jsonDecode(json));
  String encodedJson = jsonEncode(obj.toJson());
  print(encodedJson);//{"anInt":1,"aDouble":2.3,"aString":"hello","aBool":false,"anObj":{"name":"x","age":18.0}}
```

![reademe](readme.png)
