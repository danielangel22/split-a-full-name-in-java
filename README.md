# split-a-full-name-in-java
**This is an example repo in which it is proposed how to divide a full name into names and surnames, it is subject to improvements**
## Preview

![image](https://user-images.githubusercontent.com/49423514/162037953-92b4977c-7be9-42c6-a3e8-197550e12660.png)

## Code

```java

    var names = "Morales de Perez Rosalia Juana";
		var arrayNames = names.split(" ");
		var contains = arrayNames.length;
		var name = "";
		var lastname = "";
		var isMarried = Arrays.asList(arrayNames).contains("de");
		switch (contains) {
		case 2:
			name = arrayNames[0];
			lastname = arrayNames[1];
			break;
		case 3:
			if (isMarried) {
				lastname = arrayNames[0].concat(" ").concat(arrayNames[1]);
				name = arrayNames[2];
			} else {
				lastname = arrayNames[0].concat(" ").concat(arrayNames[1]);
				name = arrayNames[2];
			}
			break;
		case 4:
			if (isMarried) {
				lastname = arrayNames[0].concat(" ").concat(arrayNames[1]).concat(" ").concat(arrayNames[2]);
				name = arrayNames[3];
			} else {
				lastname = arrayNames[0].concat(" ").concat(arrayNames[1]);
				name = arrayNames[4].concat(" ").concat(arrayNames[3]);
			}
			break;
		case 5:
			if (isMarried) {
				lastname = arrayNames[0].concat(" ").concat(arrayNames[1]).concat(" ").concat(arrayNames[2]);
				name = arrayNames[3].concat(" ").concat(arrayNames[4]);
			} else {
				lastname = arrayNames[0].concat(" ").concat(arrayNames[1]);
				name = arrayNames[4].concat(" ").concat(arrayNames[3]).concat(" ").concat(arrayNames[4]);
			}
			break;
		case 6:
			lastname = arrayNames[0].concat(" ").concat(arrayNames[1].concat(" ").concat(arrayNames[2]));
			name = arrayNames[3].concat(" ").concat(arrayNames[4]).concat(" ").concat(arrayNames[5]);
			break;
		default:
			name = names;
			break;
		}
		System.err.println(lastname);
		System.err.println(name);
```
