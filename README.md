# Jonmod2 Open Standard
Accessible and Aesthetic Text Variation

# Purpose
Jonmod2 is an open text-styling standard designed to enhance readability, particularly for individuals with dyslexia, while introducing subtle aesthetic variation for general use. It balances accessibility and visual appeal by applying strategic Unicode substitutions, diacritics, and controlled spacing.

# Reasoning Behind Jonmod2
Accessibility: Inspired by dyslexia-friendly fonts, Jonmod2 provides visual cues that help distinguish similar-looking letters (e.g., b, d, p, and q).
Aesthetic Diversity: Adds stylistic variation using diacritics, glyphs, and spacing while avoiding excessive chaos (e.g., Zalgo text).
Universal Readability: Ensures legibility for all audiences by maintaining intuitive substitutions and subtle modifications.

# Intended Effect
Enhanced Readability: Reduces confusion for dyslexic readers by visually differentiating letters.
Aesthetic Customization: Creates visually distinct text for creative purposes, such as branding or social media.
Balanced Design: Avoids over-stylization, ensuring text remains functional and professional.

# Key Style Guidelines
Unicode Substitution: Replace standard letters with visually similar Unicode characters, prioritizing substitutions that preserve the original shape and sound.
Strategic Diacritics: Add accents sparingly to high-frequency letters (e.g., e, t, a). Avoid using more than one diacritic per letter.
Controlled Spacing: Introduce slight spacing between certain letters to reduce visual crowding.
Avoid Over-Styling: Maintain clarity and intent of the original text.

# Implementation Details
Letter Frequency: Common letters (e.g., e, t, a) receive subtle variations.
Dynamic Styling: Variations are randomly applied to create unique outputs.
Unicode Compatibility: Ensures substitutions work across platforms.

# Reference Python Implementation
```import random

def jonmod2(text):
    similar_chars = {
        'a': ['a', 'á', 'ä', 'å'],
        'b': ['b', 'ƀ', 'ḃ'],
        'c': ['c', 'ç', 'č', 'ċ'],
        'd': ['d', 'ð', 'ď', 'ḋ'],
        'e': ['e', 'é', 'è', 'ë', 'ē'],
        'g': ['g', 'ǵ', 'ģ', 'ġ'],
        'h': ['h', 'ĥ', 'ȟ'],
        'i': ['i', 'í', 'ì', 'ï', 'ī'],
        'l': ['l', 'ł', 'ľ', 'ļ'],
        'n': ['n', 'ñ', 'ň', 'ņ'],
        'o': ['o', 'ó', 'ò', 'ö', 'ø'],
        'p': ['p', 'þ', 'ƥ'],
        'r': ['r', 'ŕ', 'ř'],
        's': ['s', 'š', 'ş'],
        't': ['t', 'ť', 'ţ'],
        'u': ['u', 'ú', 'ù', 'ü', 'û'],
        'v': ['v', 'ṽ'],
        'w': ['w', 'ŵ'],
        'y': ['y', 'ý', 'ŷ', 'ÿ'],
        'z': ['z', 'ž', 'ź', 'ż']
    }
    styled_text = ""
    for char in text:
        if char.lower() in similar_chars:
            styled_char = random.choice(similar_chars[char.lower()])
            styled_text += styled_char
        else:
            styled_text += char
    return styled_text

Example Usage
print(jonmod2("Example Text"))

# Standard Definition
Compatibility: Text styled in Jonmod2 should be legible on modern platforms supporting Unicode.
Minimum Changes: At least 25% of the letters in the text must be altered to qualify as Jonmod2.
Preservation: The meaning of the original text must remain clear and intact.

# Licensing
MIT License

Copyright (c) 2025 Jonmod2 Project

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"),
to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
IN THE SOFTWARE.
