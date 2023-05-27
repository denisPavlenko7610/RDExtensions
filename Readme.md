# RDTools
[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://github.com/denisPavlenko7610/RDTools/blob/master/LICENSE.md)

- Use RDExtensions nameSpace and periodically update the package 🙂


## GameObject extensions

```c#
gameObject.GetOrAddComponent<Rigidbody>();

gameObject.SetParent(newObject);
```
## List extensions
```c#
private IList<string> list = new List<string>() { "string1", "string2", "string3" };
list.Random(); // return random Ilist element

list.Shuffle();  // shuffle elements

list.RemoveRandom(); // remove random element

list.IsNullOrEmpty(); // check is list empty or null

```
## Transform extensions
```c#

transform.DetachChildren(); // destroys all clildren of this transform

```

## Vector Extensions

```cs
// Simple Vector to VectorInt conversions

Vector2 vector2 = new Vector2(2f, 4.2f);

vector2.ToVector2Int(); // returns Vector2Int(2, 4);

Vector3 vector3 = new Vector3(5.2f, 3f, -1f);

vector3.ToVector3Int(); // returns Vector3Int(5, 3, -1);

// With and Add

Vector3 ourVector = new Vector3(4.3f, -3.5f, 0.2f);

ourVector.WithX(41f); // returns Vector3(41f, -3.5f, 0.2f);
ourVector.WithZ(84f); // returns Vector3(4.3f, -3.5f, 84f);

ourVector.AddX(100f); // returns Vector3(104.3f, -3.5f, 0.2f);
ourVector.AddY(100f); // returns Vector3(4.3f, 96.5f, 0.2f);

// Invert

Vector2 myVector = new Vector2(1f, 1f);

myVector.Invert(); // returns Vector2(-1f, -1f);

myVector.InvertX(); // returns Vector2(-1f, 1f);
myVector.InvertY(); // returns Vector2(1f, -1f);
```

## Color extensions

```c#

Color color = Color.green;
            
color.SetFullAlpha();

color.SetAlpha(0.5f);

color.SetNoAlpha();

```

## String extensions

```c#
myString.ToUpperFirstChar();

myList.GetRandomObject();

```

## With Extensions

```c#

bool isTrue = true;
int someValue = 20;

Instantiate(newObject)
    .With(x => x.transform.localPosition = Vector3.zero)  // add chain to set some params
    .With(x => x.transform.rotation = Quaternion.Euler(0, 90, 0), isTrue)  // add condition value with some bool param
    .With(x => x.transform.localScale = Vector3.one, someValue > 10);  // or add condition with some expression

```



