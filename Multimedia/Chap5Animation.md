# Animation
> Animation can be considered as ***PINNACLE (peak)*** of multimedia

### Animation draws inspiration from each of the other medias

### Computer became a partner in creative expression
- Lowered costs
- Made creating animation easier
- Supports creative expressions through:
    - Interactivity
    - 3D sensory experience
    - Embodiment and implementation of rules of behavior

# Table of Contents
1. [Animation Basics](#animation-basics)
2. [Traditional Animation](#traditional-animation)
3. [2D animation](#2d)
    - Keyframe and Tween (Under [Animation Software and 2D in general](#2d))
    - [Programmed](#programmed-animation)
4. [3D animation](#3d)
    - [Motion Capture](#motion-capture)
    - [Kinematics](#forward-kinematics)
    - [Animating With Physics](#animating-with-physics)
5. [Guidelines for Animation](#animation-tips-and-guidelines)

# Animation Basics

### Animation
> Rapidly displayed sequence of individual still images made possible by ***PERSISTENCE OF VISION***

### Persistence of vision
- Images formed on the retina persists for a short period of time after the stimulus has disappeared
- This physical memory of the retina will produce the illusion of motion if a bunch of connected still images are displayed fastly

### Early animating devices
- Thaumatrope

    ![Traumatrope example](./imgRes/mtm_c4_thaumatropejpg.jpg)

- Zoetrope

    ![Zoetrope example](./imgRes/mtm_c4_zoetrope.webp)

### Flipbook technique
- Still Images showing a different stage of a motion are created (drawn or printed) on different pages
- The pages are flipped through rapidly, and because of ***PERSISTENCE OF VISION*** our eye are being tricked to connect those still images and link them into a motion
- Animation basics used in flipbook:
    - Quality of motion -> based on rate of display
    - Speed -> based on the differences between images
    - Onionskinning -> a technique to draw new image based on the previous image via ways like tracing
    - Registration -> physically aligns images with one another

# Traditional Animation

### Film based process
- Images are photographed and recorded as separate frames on a long strip of transparent film
- With the help of a light source, the films are shown on a screen and when a series of films are shown in that way, the illustration of motion happens

### Film enhanced the possibilities of animation
- Multiple reels (like the big big wheel that has films wrapped around it) allowed longer animations
- Projectors are able to display the images at a reliable frame rate
- Animators could add sound to the motion

### Challenges of traditional animation
- Number of images to create very many
    - 24 frames per second requires 1440 still images for one minute of the animtion
    - Methods to generate images (and to solve this problem) include:
        - Shooting on two -> cuts number of images in half
        - Cycle ofimages are reused to extend repetitive motion
        - Holds -> produce sequence of identical drawings to extend a particular state of action
- Artistic strategies to create realistic world require:
    - Awareness of how things move in the real world
        - Ease-in (start slow end fast) and ease-out (start fast end slow) helps to address the physics of motion
        - Overshooting a resting point shows kinetic energy of motion (it's like you let the thing go over where it's supposed to go and then pull it back)
        - Overlapping motion -> different components move independently on its own
    - Exaggerate motion for dramatic effect
        - Different speeds are used
        - Stretch and squash technique are used -> the ball are squashed as it hits the ground and stretched when it's bounced back up

# Traditional motion techniques

### Strategies for achieving motion has been applied to
- Paper cut-outs
- Clay figurines
- Puppets
- Natural objects photographed, reposed, then re-photographed again

# CEL Animation

### CEL Animation is perfected and made popular by Disney studios

### This technique directly influenced development of digital animation

### CEL
- Drawings made on sheets of celluloid
- Drawings were then photographed to produce the animated film

### Advantages
- Artists save drawing time
    - ***Fixed*** components of a scene were drawn once and ***LAYERED*** on the bottom of a stack of celluloid sheets
    - ***Moving*** components are drawn separately and then placed on top of the fixed scene components
- Precise control over elements
    - Individual cel layers can reproduce ***independent, complex*** motions
- Encouraged division of labor and promoted high artistic standards
    - Master artists draw the ***key frames or the extremes***
        - Key frames or extremes -> The state of the character and the scene at a certain time
    - Assistants draw the ***tweens***
        - Tweens -> The transition frames between two keyframes
    - Inkers transfer the drawings from paper to celluloid
    - Opaquers apply colors to the celluloid
    - Other specialists
        - Producer
        - Directors
        - Script writers
        - Audio specialists
        - Camera operators
        - Checkers

### To produce CEL animation
- Cost and complexity of creating animation requires a carefully defined process
- Storyboard
    - Sequence of drawings that sketches out content of major scenes in production
- Pencil Test
    - Series of simple sketches that are photographed and projected to test the design of animated sequences
- Scratch track
    - Draft of animation's audio track
- Leica reel
    - Working draft of the complete animation
- Uses ***specialized*** equipment in production
    - Specialized paints to convey proper hue (or color)
    - Specialized camera and lighting to capture cels
    - Specialized device to
        - Track changes in paths of animated characters
        - Align and hold the cels for camera shots
        - Synchronize and edit the final film
- Cel animation is a complex, demanding and expensive animation
    - The appearance of computer improved the process

# Digital Animation

### Two different forms
- [2D](#2d)
- [3D](#3d)

# 2D
- Evolved from traditional animation techniques
- Produced by mimicking basic traditional animation techniques like
    - Flipbook technique
    - Cutout animation technique
    - Rotoscoping
    - [CEL animation](#digital-cel-animation)
- Paint/draw programs are used to create the components
- [Animation softwares](#animation-softwares) can sequence, set timing, transitions and produce the final animation

### Digital CEL Animation
- Animations are a series of individual frames
- Synchronized to one or more sound tracks
- Graphics arranged on layers
- Major changes identified in keyframes
- Illusion of motion produced as series of tweens
- [Go Back](#2d)

### Animation Softwares
- Elements of Flash organization
    - Timeline: Horizontal row of frames
    - Frames: Multiple layers in columns
        - Layers stack and have order
            - Lower layer: Background elements
            - Higher layer: Changing elements
    - Keyframes: Major changes in a frame
    - Tweens: Frames created automatically by software (although this two applies to Flash, it's actually the same thing, just that the Flash will help you create Tweens)
    - Onionskinning: Assists in drawing changes from one frame to the next
- Frame-by-frame animation
    - Each frame is manually drawn to reflect motion sequence
    - Detailed control of each motion
    - Very VERY time consuming
- Tween animation:
    - Computer generates the frames between two keyframes
    - Some examples are (lazy explain if out then unlucky or just memorize)
        - Motion tween
        - Path based tween
        - Shape tween (morphing)
        - Size tween
        - Color tween (I giv color tween eh example, applies to other tween as well)
            - Computer generates in between, transition color from the first color to the second color specified by the keyframe
        - Transparency tween
- Provides tools to support animation process
    - Image editing tools
    - Alignment tools and grids
        - To control placement
    - Text tools
    - Basic sound control
    - Strategies to support interactivity
- [Go Back (to 2D)](#2d)

### Programmed animation
- Animators write commands
- The computer generates the animation based on the commands
- Requires knowledge of programming and mathematical techniques to specify the motion
- Advantages
    - Smaller file size
    - Animations load and play faster
    - Reduces bandwidth and processor demands
    - Efficient in creating different versions of animated sequence
    - Supports complex forms of interactivity
        - Computer can receive input from the user and animate the game objects on the spot
- Scripting languages frequently used to generate programmed animations
    - Lingo
    - JavaScript
    - ActionScript

[Back to Forms of Digital Animation](#two-different-forms)

# 3D
- Exploited capabilities unique to computer
- Elements of 3D animation that can be set in motion
    - Objects
    - Sounds
    - Camera
    - Light
- Techniques are similar to 2D animation:
    - Keyframes
    - Tween motion
- Complex motion may involve using models of humans or animals

### Motion Capture
- Also called *performance animation*
- Technique of recording motion of real life objects, then map them to a computer generated character
- Performers will have sensors dedicated to track the motion of various body parts as they create the action sequences
- Primararily used to capture motions that are hard to be created

### Forward Kinematics
- ***Kinematics*** (same applies to [Inverse Kinematics](#inverse-kinematics))
    - Study of motion of bodies or system of bodies
    - Motion of one part generates related motion in other parts
- Animators will need to adjust all motion in all related parts of the body
- Advantages
    - Models easily defined
    - Computer processing is minimal
    - Simple to implement
- Disadvantages
    - Quality of motion depends on animator's skill
    - Very time consuming

### Inverse Kinematics
- Software knows and applies the knowledge of anatomical motion
- Advantages
    - More realistic than Forward Kinematics
    - Simplifies animator's work and ensures consistent motion
    - Reduces work of animator
- Disadvantages
    - Requires innovative programming
    - Requires more power than forward kinematics

### Animating with Physics
- Software generate motions based on properties of object and law of physics
- Frees animators from tedious tasks of 3D animation and can produce more realistic content
- Animators will only need to focus on developing stories and characters

### Rendering
- Final step to complete the animation
- Applies
    - The modelings
    - Surface definitions (or textures)
    - Scene compositions as specified by the animator
- Options
    - Prerender
        - Require large processing resources and time for animated movies
        - Computer carry out complex calculations to implement object properties, lighting, camera angles and motions
    - Realtime rendering
        - Computer produces animation immediately
        - Used in video games and highly interactive 3D animations

[Back to Forms of Digital Animation](#two-different-forms)

# Animation Tips and Guidelines
- Prepare for a learning curve
    - Animation programs are difficult to master
- Design for delivery
    - Minimize the file size if the delivery is for the Web
- Consider clip animation to reduce cost (I have no idea what is Clip Animation also)
- Consult the tradition in developing motion
    - Cycles
    - Holds
    - Shooting on twos
    - Tweening
    - Stretch and squash
    - Overshoot and overlap motions
