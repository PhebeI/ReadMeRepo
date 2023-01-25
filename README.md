# Project History

This project details all our projects that have been deployed to Github.

## Project Information

This describes our projects and their importance and what it does.

```bash
project name: xmlwrangler
description: taskXML is a Python file for manipulating a movie xml file.
Usage: python taskXML.py
![xmlwrangler_shot](https://user-images.githubusercontent.com/119197163/214538067-028b57b1-67dc-451d-8e8a-2f5dd46a7ae7.PNG)
```
```bash
project name: MyCV
description: Details profile, work experience, training and place of origin.
Usage: https://phebei.github.io/MyCV/
![my_bio_shot](https://user-images.githubusercontent.com/119197163/214538483-9bece26b-af6d-4964-aae9-569e9ad53385.PNG)
```
```bash
project name: modestapparel
description: clothing website about royal and modest apparel.
Usage: https://phebei.github.io/modestapparel/
![modestapparel_shot](https://user-images.githubusercontent.com/119197163/214538733-9bee0ca5-fbca-4691-9b85-3c6cad8420cd.PNG)
```

# xmlwrangler

taskXML is a Python file for manipulating a movie xml file.

## HowTo

```bash
python taskXML.py
```

## Usage

```python
import xml.etree.ElementTree as ET

# gets the root of the xml file
tree = ET.parse('movie.xml')
root = tree.getroot()

# prints tags of the movie element
for movie_elem in root.iter('genre'):
    print(movie_elem.tag)

# prints movie descriptions
for movie_desc in root.iter('description'):
    print(''.join(movie_desc.itertext()))

# prints favorite and non-favourite movies
for movie_fav in root.iter('movie'):
    print(movie_fav.attrib)
```
