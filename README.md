# What Are Vectors in machine learning?

Imagine you want to teach a computer the meaning of words. How would you do it? You can't just feed it a dictionary definition—computers don't understand language like humans do. This is where vector embeddings come in.

## What Are Vector Embeddings?

Vector embeddings represent data—like words, images, or documents—as points in a multi-dimensional space. Each dimension reflects a feature or characteristic of the data, and the position of a point reflects its meaning and relationships to other points.

## Think of It Like a Map

Imagine a map where cities are placed based on their geographical features:

- One axis represents the distance from the equator (latitude)
- Another axis represents the distance from a prime meridian (longitude)
- A third axis represents altitude
- Cities with similar features (e.g., close to the equator and at sea level) cluster together

Vector embeddings do something similar with data:

- Instead of cities, we have words, images, or other data points
- Instead of geographical features, we use features that capture the meaning or characteristics of the data
- Similar data points cluster together in this multi-dimensional space

## Example With Animals

Let's represent "dog," "cat," and "wolf" as vectors in a multi-dimensional space. Each dimension reflects a characteristic like size, habitat, or diet:

Dog: Medium-sized, lives on land, omnivorous diet  
Cat: Small-sized, lives on land, carnivorous diet  
Wolf: Medium-sized, lives on land, carnivorous diet

In vector form:

```
Dog: [medium, land, omnivore]
Cat: [small, land, carnivore]
Wolf: [medium, land, carnivore]
```

The relationships between these vectors reveal their similarities:

- "Dog" and "Wolf" are closer because they share more traits
- "Cat" is further from "Wolf" due to differences like size and solitary behavior

This example shows how relationships can be encoded in space, scaling to abstract data like language.

## From Animals to Sentences: Translating Language

Just as the relationships between "dog" and "cat" are captured in vector space, relationships between words in a sentence can also be encoded this way. For example:

English: "The cat sits on the mat."  
Spanish: "El gato se sienta en la alfombra."

### Words as Vectors

Each word is represented as a vector encoding its meaning, grammatical role, and context. These relationships allow models to:

- Map "cat" to "gato"
- Map "sits" to "se sienta," while adapting to Spanish grammar
- Map "on the mat" to "en la alfombra"

By preserving these relationships in vector space, the model generates accurate translations.

## How Are Vector Embeddings Created?

Vector embeddings are created through a combination of human guidance and machine learning.

### 1. Human Guidance

- Selecting Relevant Features: Data scientists identify important characteristics (e.g., size, habitat for animals; grammatical roles for words)
- Creating a Training Dataset: Humans curate labeled datasets (e.g., animal descriptions or sentences showing word usage)

### 2. Machine Learning

- Learning Patterns: Neural networks are trained on the dataset to identify patterns and relationships
- Generating Embeddings: The model converts each data point (e.g., an animal or word) into a vector, with dimensions representing learned features

## Code Example: Creating Vector Embeddings for Animals

Here's a simple Python example to structure data for embeddings:

```python
# Create a dictionary to store animal data
animal_data = {
    'animal': ['elephant', 'dolphin', 'sparrow', 'giraffe', 'shark', 'eagle', 'cat', 'dog'],
    'size': ['large', 'large', 'small', 'large', 'large', 'medium', 'small', 'medium'],
    'habitat': ['land', 'water', 'air', 'land', 'water', 'air', 'land', 'land'],
    'diet': ['herbivore', 'carnivore', 'omnivore', 'herbivore', 'carnivore', 'carnivore', 'carnivore', 'omnivore'],
    'covering': ['skin', 'skin', 'feathers', 'skin', 'skin', 'feathers', 'fur', 'fur']
}

# Convert the dictionary to a Pandas DataFrame
import pandas as pd
df = pd.DataFrame(animal_data)

# Print the DataFrame
print(df)
```

Output:
```
    animal     size  habitat       diet   covering
0  elephant   large     land  herbivore       skin
1   dolphin   large    water  carnivore       skin
2   sparrow   small      air  omnivore   feathers
3   giraffe   large     land  herbivore       skin
4     shark   large    water  carnivore       skin
5     eagle  medium      air  carnivore   feathers
6       cat   small     land  carnivore        fur
7       dog  medium     land  omnivore        fur
```

This structured data helps the model learn patterns and generate meaningful embeddings.

## Why This Matters

By combining human intuition with machine learning, vector embeddings scale from understanding simple relationships (like animals) to performing complex tasks (like language translation). This foundational concept drives advancements across diverse fields.

## Vectors in Adobe Illustrator

While visual vectors in tools like Adobe Illustrator aren't the same as machine learning embeddings, they share the same mathematical foundation: representing data as numbers in space. Learn more about [vectors in Adobe Illustrator here](illustrator-vectors.md).
