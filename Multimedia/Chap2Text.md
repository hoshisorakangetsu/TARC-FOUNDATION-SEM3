# Power of Text
- Clarity
- Universality
- Efficiency
- Abstraction, engagement and suggestion

# Text Tradition

### Typeface
- Family of characters that share a common design
- Commonly categorized as
    - Serif
    - Sans Serif
    - Script
    - Symbols

### Style
- Appearance of characters:
    - **Bold**
    - *Italic*
    - <u>Underline</u>
- Point (pt)
    - Commonly used as a unit for font sizes
    - approximately 1/72 of an inch
- Pica
    - 12pt

### Font
- Complete set of characters of a particular typeface, style and size
- Monospaced fonts
    - all characters are of the same width
- Proportional fonts
    - width of the characters are adjusted based on the shape

### Case
- Uppercase
- Lowercase

### Weight
- Line thickness of the typeface
- Higher weight means more bolded words

### Kerning
- Adjust the spacing between ***SPECIFIC*** letters

### Tracking
- Adjust spacing between ***ALL*** characters

### Condensed/extended text
- Text with a ***narrow*** / ***wide*** width

### Leading
- Spacing between lines

### Alignment
- Position text relative to document's margins

### Justification
- Adjust line length to produce straight edges on left and right margins

# Computer Text
> Coding schemes assign a group of binary numbers to represent a digital character

### ASCII (American Standard Code for Information Exchange)
- 7-bit code -> 128 characters
- Extended ASCII (ASCII-8) -> 256 characters
- Understanded by ***ALL*** computers

### RTF
- Developed by Microsoft aiming for cross platform text files
- Able to reproduce the original file's formatting

### Unicode
- New standard of 16 bit code that provides more than 65,000 characters
- Goal is to include multilingual text in a single digital coding standard

# Font Technologies

### Bitmapped fonts
- a "mapping" of a character
- Pixels that make up the letter are described in a binary code
- Every character is stored as a bitmapped letter, number or symbol
- Requires large memory and storage capacity
- Advantages
    - Precise control over letter appearance
    - Letters can be edited at pixel level just like images
- Disadvantages
    - Letters cannot be easily scaled (quality will be ruined)
    - separate bitmaps are reuired for every different typefaces, styles and point sizes
    - requires large storage capacities
    - limited flexibility in use of text fonts to those stored on the computer

### Outlined fonts
- a ***DESCRIPTION*** of the character to be displayed is stored
    - Description: a series of command to create the letter on computer display
- Technologies
    - Adobe PostScript
    - TrueType (more common)
- Advantages
    - Can be scaled easily
    - little storage capacity is needed
- Disadvantage
    - Commands are hard to be edited to create unique characters
    - Font families are controlled through the license of Postscript and TrueType fonts

# Jaggies
- Jaggies are defined as text squares that display curve or diogonal lines produce a stair-stepped effect (the pixelated edges produced when u zoom in on a text alot)
- Jaggies produce an alias of the true character

### Anti-aliasing the jaggies
- Creates a smooth edge by blending the color of the text with the color of the background

# Installed Fonts

### Problems
- ASCII and UNICODE are standard
- Fonts installed locally are not standardized across computer platforms
    - if the font is not available on the computer, the computer will substitute another font in and may cause the result to be unacceptable

### Solutions
- Use only widely available fonts
- Package the unique font together with the application

# Multimedia Text

### Editable
- Text produced by word processor or text editors
    - Contents are easily altered
    - Spell check and search is available to use

### Graphics
- Image of a text that can be manipulated to produce a wide range of artistic effects
    - Original word picture can be made
    - Problems of installed fonts are solved
        - unique fonts don't need to be packaged as the text already exist as a picture

# Multimedia Text & Sound

### Speech recognition (AKA Speech To Text)
- Software analyzes human speech and converts words to editable text
- Specialized "intelligent" software is required
- Accuracy depends on training and the speaker's voice

### Speech synthesis (AKA Text To Speech)
- Software analyzes text and reproduces it as spoken words

# Text and Interactivity

### Hyperlink
- Linked text
- User interacts with links to trace relationships of words and ideas created by the author

### Structures
- Nodes (as in elements? I guess)
- Link anchor (as in the real link that the user will be navigated? I guess)
- Link markers (as in the thing to be pressed by the user to send the user to the Link anchor? I guess)

### Hypermedia
- Information structure based on linked media

# Text for the WWW

### HTML (HyperText Markup Language)
- Contains ***tags*** used to specify the structure of the document and formats the text and media
- Browsers have the ability to intepret the ***tags*** and display the page as the author intended on the client's device
- Limitations
    - limited set of tags to create a page (firendly reminder: this is not the case anymore now)
    - Hard to define a page appearance precisely
        - different browsers and computers may have different way of intepreting the tags and present the page differently

### CSS (Cascading Style Sheets)
- Addition to HTML
- Separate content of page from formatting codes
- Style the page to be more visual appealing
- Easier to edit and maintain the consistency of appearance of a site

### XHTML (eXtensible HTML)
- Blends HTML and XML
- XML allows powerful data manipulation
- Improves page display on mobile devices

# PDF (Portable Document Format)
> Maintains original formatting of documents across computer platforms
- Platform and application independant
- support multiple medias and user interaction
- requires a ***READER*** to view the file and an ***ENCODER*** to convert a document to PDF
    - Most web browsers now come with a built-in PDF reader
    - Adobe Acrobat Reader is a free reader
    - PDFCreator is a free and open sourced encoder

# Add Text to Multimedia Application
- Direct entry in a text box or text field
- Copy paste from existing text source
- File import for large text files
- Scan text with OCR application for text that only exist in printable media
    - ***OCR (Optimal Character Recognition)***: accuracy varies based on fonts and quality of source material

# Guidelines for Text in Multimedia Applications
- Be selective
- Be brief
- Make text readable
- Be consistent
- Be careful and respectful
- Combine text with other media
- Make text interactive
