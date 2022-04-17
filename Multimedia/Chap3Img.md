# Graphics
> Wide range of pictorial representations from simple line drawings to blue prints, charts, logos, paintings, photos, animation and movies
### My own take
> Graphics is an image/video representation of text. It is normally used to represent texts and the meanings that a person wants to convey. Graphics are generally easier to understand.

# Challenges of Computer Images
- Large file size
- Slow downloads and processing
- Possible inferior (lower) quality than the original
- File format compatibility
- Images are displayed differently on different monitors and printers

# Contone Image
- FUN FACT: Contone stands for ***Continuous Tone***
- Composed of ***CONTINUOUSLY VARYING SHADES*** of color
- A traditional black and white contone image is made up of continuously varying shades from white to gray to black

![Contone Image Example](./imgRes/mtm_c2_contone.png)

# Line art
- Combination of lines to make images
- Uses only ***TWO*** colors
    - 1 for the line (foreground)
    - 1 for the background

![Line Art Example](./imgRes/mtm_c2_line_art.jpg)

# Black and White Image Reproduction
> Images made with a series of ink dots

### Linescreen
- lines per inch
- designates the size of the dots and quality of resulting image
    - 150 lpi is better than 85 lpi

![LPI Visuaization](./imgRes/mtm_c2_lpi.jpg)

### Halftones
- Form image by ***CLUSTERING*** ink dots
- tight cluster of black and white dots are capable of creating dark gray
- loose cluster of black and white dots can create lighter gray

![Halftone Image](./imgRes/mtm_c2_halftone.jpg)

# Color Image Reproduction
> Uses a series of four-color dots with transparent inks

### CMYK
> Cyan, Magenta, Yellow and Key (usually black) (blame github for not supporting markdown colors)
- small dots of different color combinations can reproduce more different colors

### ***Subtractive***
- often used to form color images on printed surface
- Light is ***REFLECTED*** frome the printed surface
- Pigments that form the image absorbs some of the colors
- The remaining colors reach our eye to produce the image

### ***Additive***
- Often used to form color images on computer monitor
- the ***RGB (Red Green Blue)*** color model
- Varying amounts of Red, Green and Blue light are added together ro create the color

> Additive Color models (RGB) are converted to  Subtractive color models(CMYK) if the image is going to be printed

# 2D Computer Graphics

### Bitmapped graphics
- Created as a pattern of discrete elements
- Each element is a ***PIXEL*** or "picture element"
    - Pixel:
        - Small squares
        - Assigned a binary code to define the color
        - More bits assigned = more binary length = more color possibilities = more details
- Categories:
    - Line art 
        - Produced using 2 colors (usually black and white)
        - Advantages:
            - Clear, crisp image
            - Small file size
        - Uses:
            - Chart
            - Illustration
            - Diagrams
    - Grayscale
        - produced using shades of gray
        - generally ***8-bit*** images of 256 shades of gray
        - Advantages:
            - Nice representation of black and white photos
            - Smaller file size than full color
            - Lower printing cost than color
        - Uses: image that require more detail than line art
    - Color 
        - produced with patterns of colored pixels
        - ***BIT DEPTH***: 
            - number of bits used to encode each pixel
            - determines the color possibilities
        - photo-realistic color requires 24-bit color
    
# Making computer colors

### 2 ways in general:
- identify a table of possible colors for the computer
- specify varying amounts of Red, Green and Blue

### 8-bit color
- a specific range of colors in a table
- PCs and Macs use different tables
- ***Web-safe*** table provides color that will display the same on all platforms

### 24-bit color
- combines 8-bit values of red, green and blue to create the result
- 16.7 million color possibilities
    - FUN FACT: 48-bit color has 16-bit values with 281 TRILLION color possibilities

# Bitmapped Image Quality
> Depends on TWO factors (spatial resolution and color resolution)

### Spatial resolution
- density of pixels per inch
- measured in ***PPI(Pixels Per Inch)*** for monitor output
- measured in ***DPI(Dots Per Inch)*** for print output
- Higher spatial resolution
    - more detail (pixels are smaller and closely packed)
    - sharper and more accurate images are produced
    - LARGE file size but better image quality
- Lower spatial resolution
    - less detail (pixel are larger)
    - image appears to be fuzzy
    - small file size, but lower image quality

### Color resolution
- number of colors each pixel can display
- determined by bit depth
    - low bit depth = small file size = less color
    - high bit depth = large file size = more color
- low color resolution may cause ***COLOR BANDING*** and ***QUANTIZATION***
    - Color banding
        - a subtle form of ***POSTERIZATION***, which converts a continuous gradation of tone to several regions of fewer tones
        - while posterization is done for artistic effects, color banding is an unwanted artifact
        - caused by rounding of the color of each pixel to the nearest digital color levels (often because the limitation of the display device)
        - Color banding effect can be seen on the sky of the image below
        ![Color Banding Example](./imgRes/mtm_c2_colorBanding.jpg)
    - Quantization
        - Happens when a range of values are being compressed into a single quantum value
        - may lead to break in shades of continuous tone images (like color banding)
- Indexing
    - Specific pallette of colors is identified to optimize the appearance of lower color resolution image
    - Methods:
        - Adaptive
        - Perceptual
- Dithering
    - Combine pixels of different colors to produce another color that is not available in the indexed palette
    - Improves image quality without increasing bit depth
    - Capable of solving the problem of quantization and color banding (by creating the transitional color on the hard stops [if this is chim sila ignore XD])
    - ![Dithering](./imgRes/mtm_c2_dithering.png)
    - *if you zoom in on the photo you can see small dots on the dithered image*

### Device dependence
- dimensions of an image depend on the resolution of the output device. 
- Monitors generally have lower spatial resolution (again, idk if this is still the case now)
    - Mac: 72ppi
    - PC: 9ppi
- Printers generally have higher spatial resolution: 300dpi to 2400dpi
- bitmapped images are device-dependent:
    - 300ppi image prints the original size on a 300ppi printer
    - 300ppi image is greatly enlarged on a 72ppi monitor

# Resampling Bitmapped Image
> Process of increasing or decreasing the number of samples described in a file (changes the original image)
- Often used to control spatial resolution of bitmapped images (rmb how 300ppi image will be shown on a 72ppi monitor?)
    - 72ppi for web display
    - 300 ppi for laser output

### Upsampling
- Adds samples to the file
- Used to ***ENLARGE*** the physical dimensions of an image on a given device
- Softwares have special algorithms to ***interpolate*** the pixel and color to be added to the image, the interpolated pixels and colors are then ***CREATED*** by the software for the image
- The more data is added, the more the image is ***DEGRADED*** via upsampling
- It is just nearly impossible to blow a 72ppi image to 300ppi (now gt AI its not tht pain staking anymore tho but notes dh)

### Downsampling
- Reduces samples from the file
- Can produce smaller images but still maintain good quality

### Best practice
- Capture at ***HIGHEST*** possible spatial resolution when possible
- Only downsample as needed for different usages of the image

# Resize Without Resampling
> It is possible to resize a bitmapped image without resampling

### Enlarging a printout ***CAN*** produce acceptable results
- ***BUT:*** excessive enlargement will distort the image with ***blocky, mottled surface***
![Excessive Enlarging](./imgRes/mtm_c2_enlargeWOResampling.jpg)

### Reducing the image size without resampling can produce high quality printouts
- Pixels are ***packed more closely*** to each other

### Resizing without resampling has no effect on monitor display of image
![Resize Without Resampling](./imgRes/mtm_c2_resizeWOResampling.png)

# Sources of Bitmapped Images

### Paint programs
- Specialized software for creating bitmapped images
    - Adobe Photoshop
    - MS Paint
    - GIMP
    - Inkscape
    - Krita

### Digital cameras
- Number of pixels sampled by the camera is the camera's spatial resolution
- Measured in megapixels

### Scanner
- Capture existing or original art image
- Capture 3D objects

### Clip art
- Royalty free
    - Once the initial use is permitted (some require you to pay for the initial usage, some is free), the subsequent uses are free (no matter how you use it)
    - Licensed usage (you may need to renew your license to use it on different fields)

### Screen grab (AKA Screenshot)
- Save image on a monitor to a bitmapped file
- Spatial resolution is generally low

# Bitmapped File Formats
- PICT
- PNG
- BMP
- GIF
- TIFF
- JPEG

### Compression
- Lossy
    - Removes redundant or unneeded details or informations or datas in the file, reducing the file size
    - File compression formats:
        - JPEG
        - MP3
- Lossless
    - Relies on statistical redundancy to store data without losing any information
    - Reversible
    - File compression formats:
        - PNG
        - GIF

# Vector drawn graphics

### Vector
- A line with length, curvature and direction

### Vector graphics
- Images created from ***mathematically defined*** shapes 

### Advantage
- Can be enlarged without distortion
- Smaller file size

### Draw programs
- Program used to draw vector graphics
- Tools that resembles those of a draftsman
    - Fixed shapes
    - Bezier curves
    - Pen
- Objects are layered on each other and grouped to form complex images
    - Grouping joins individual shapes
    - Ungrouping separates the groups back into individual shapes
    - ![Vector Example](./imgRes/mtm_c2_vector.png)
    - *to the left is the illustration, to the right are the layers (This vector is created via combining diff layers)*

### Device Independence
- Vector graphics can be used on different devices without altering the image dimension (deep down vector is just a mathematical formula after all, and is calculated on the spot when it is used)
- Printers and monitors preserve the original dimension of the image

# Vector to Bitmapped & Back

### Autotracing
- Softwares analyzes a bitmapped image for shapes and converts the image into a vector graphic

### Rasterizing
- Samples the vector image and saves it in bitmapped form
- Can think of like sort of "screenshot-ing ~~(or screen grab in terms of notes)~~" the vector graphic displayed on screen

# Vector graphic file formats

### Native format
- Depends on the application used

### General purpose
- Vector-only:
    - EPS (Encapsulated Postscript)
    - PDF (Portable Document Format)
- Metafiles:
    - SVG (Scalable Vector Graphics)

# Advantages (Bitmapped VS Vector)

### Bitmapped Images
- Represent complex contones
- Full featured photo editing
- Wide range of artistic effects
- Precise Editing

### Vector Images
- Smooth scaling and reshaping
- Ease of editing objects in layers
- Small file size
- Device independent

# Disadvantages (Bitmapped VS Vector)

### Bitmapped Images
- Large file size
- Precision are lost when the image/shape is scaled or rotated
- Device dependent

### Vector Image
- Inaccurate, incomplete represent of complex contone images
- No photo-editing capability
- Limisted artistic control/effects

# 3D Computer Graphics

### Four steps
1. [Modeling](#modeling)
2. [Surface definition](#surface-definition)
3. [Scene Composition](#scene-composition)
4. [Rendering](#rendering)

# Modeling
- Process of specifying the shape of the 3D object
- Two approaches
    - Combine ***PRIMITIVE*** objects to form a new shape
        - ***PRIMITIVE*** Objects -> 3D shapes supplied by the 3D graphic programs
    - Use a ***MODELER*** to create shapes directly
- Modelling with primitives (extended ver.)
    - Use basic shapes to create complex 3D models
- ***Parametric primitives***
    - Objects that can be changed by specifying parameters like radiu
    - Primitives can be scaled, rotated, moved and combined
    - CSG (Constructive Solid Geometry)
        - Primitives are joined, subtracted from or intersected with using Boolean operators

### Modelling techniques
- [Polygon modeling](#polygon-modeling)
- [Spline modeling](#spline-modeling)
- [Metaball modeling](#metaball-modelling)
- [Formula modeling](#formula-modelling)

### Polygon modeling
![Polygon Modelling Exp](./imgRes/mtm_c2_polygonModeling.jpg)
- Object defined as pattern of straight-edged polygons
- Similar to bitmapped graphics in that the object is defined by fixed number of elements
    - Fixed number of polygons for 3D
    - Fixed number of pixels for 2D
- Advantages
    - High quality, realistic surfaces
    - Precise editing control
- Disadvantages
    - Large file sizes
    - Scaling distortions
- [Back to modelling techniques](#modelling-techniques)

### Spline modeling
![Spline Modeling Exp](./imgRes/mtm_c2_splineModeling.jpg)
- Use ***CURVES*** to create objects
- Similar to 2D vector graphics
- ***NURB*** Approach
    - Non-Uniform Rational B-spline (not in notes, google best)
    - Define an image using ***MATHEMATICAL*** formulas
    - Able to be adjusted to various shape and sizes
- Advantages:
    - Small file sizes
    - Flexible objects
    - NURBs are easily scaled
- Disadvantages:
    - Less editing control
- [Back to modelling techniques](#modelling-techniques)

### Metaball Modelling
![Metaball Modeling Exp](./imgRes/mtm_c2_metaballModeling.jpg)
- Objects created as combination of elements called ***BLOBS***
    - BLOBS
        - ***Positive*** Blobs add to the object
        - ***Negative*** blobs subtract from the object
        - Smooth like lumps of clay
- Good for objects with soft edges
- [Back to modelling techniques](#modelling-techniques)

### Formula Modelling
![Formula Modeling Exp](./imgRes/mtm_c2_formulaModeling.png)
- Create object by specifying ***MATHEMATICAL*** formulas, and is then drawn by computer
- Requires knowledge of programming and advanced mathematics
- [Back to modelling techniques](#modelling-techniques)
- [Back to Modeling Steps](#four-steps)

# Surface Definition
- Textures applied to the model's surface
- Menu choices surfaces include wood, glass, metal, skin
- Appearance of surfaces can change via altering the color, opacity and reflectivity
- Custom surfaces
    - Image maps
    - Bump maps
- [Back to Modeling Steps](#four-steps)

# Scene Composition
- Objects are arranged
- Backgrounds are defined
- Environmental effects added
- Lighting established
    ![Lighting Types](./imgRes/mtm_c2_lighting.jpg)
    - Lighting choices
        - Omni lights (also called point lights)
        - Directional lights
        - Spot lights
        - Volumetric light (also called ambient light or global illumination)
- Adjust lightig with brightness, color and attenuation
- [Back to Modeling Steps](#four-steps)

# Rendering
- Computer processes the scene specified by the artist
- Two main approaches
    - Pre-rendering
        - Render first into picture/video then use later
        - Used for:
            - Graphics
            - Animation
            - Video with limited interactivity
    - Real-time rendering
        - Renders realtime (as the name implies)
        - Used for
            - 3D applications like video games
- Forms of rendering to create test scenes
    - Wireframe rendering
        - A series of ***LINES*** used to define the shape of an object is displayed, the surface is not shown
        - Useful to test for basic geometry and placement of an object
        - ![Wireframe Example](./imgRes/mtm_c2_wireframe.jpg)
- Surface rendering
    - Applies lighting and shaders to the object
    - ***Flat Shader***
        - Imperfect but fast render process
    - ***Smooth Shader***
        - Better quality surface
    - ***Ray tracing***
        - Traces every rays of light as it interacts with objects on a scene
    - ***Radiosity***
        - Recreates the changes that result from interaction of different wavelength of light
    - ![Surface Rendering Exp](./imgRes/mtm_c2_surfaceRendering.png)
- ***Final*** Render
    - Translates 3D information to a 2D image
    - ***Rendering Engines*** apply effects to the finished products (shadows, bumps, reflections, transparencies and lighting taken into account)
    - Requires processing power, time and artistic talent to be successfull
- [Back to Modeling Steps](#four-steps)

# Creating Worlds
- 3D graphics are powerful to create reproduction of the world around us
- Fantasy worlds come alive with the help of creative artists and software applications like Maya, Blender, ZBrush #D StudeioMax

# Guidelines Using Graphics in Multimedia
- Identify the purpose of the graphic
- Choose best format for each image
- Match graphic design to purpose
- Locate graphics (? I don't really understand but it's in notes)
- Preserve the quality of image
- Economize (? I don't really understand but it's in notes)
- Organize and store graphic files for later use
