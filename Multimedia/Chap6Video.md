# Video

### Video can be perceived as ***MOVING PICTURES***
- Much like animation, videos or films are a series of rapidly displaying pictures
- Each picture captures an instance of a motion
- ***PERSISTENCE OF VISION*** helps in perception of flow of motion.

# Analog

### Analog ***FILM*** records images on transparent medium that is later projected onto a screen to replay the video

### Analog ***VIDEO*** records images as continuously varying electric voltages that produce images on a CRT or projection screen
- CRT -> Cathode Ray Tube (F5 physics eh thing I don't rlly rmb also liao but I rmb mcm has smtg to do with electrons and magnetic fields)

# Digital Video

### Digital Video Challenges
- Large file size
    - Every ***SECOND*** requires about 30MB of storage
- Hardware Performance
    - Computer processors, memory and bus size must deliver digital video to the screen at full motion frame rate
- Distribution methods
    - DVD Players
    - High speed network bandwidth
> However, it is made possible by compression algorithms, DVD storage and bandwidth as high as Gigabit

### Digital Video Quality
- 3 Factors
    - [Screen Resolution](#screen-resolution)
    - [Frame Rate](#frame-rate)
    - [Compression method](#compression-method)
- These 3 factors can be adjusted by the developer to optimize the delivery of a digital video

### Screen Resolution (Output resolution)
- Number of horizontal and vertical pixels used to present the video image
- Impacts processing, storage and transmission requirements
- High quality Digital Video(DV) format is **720x480** (or 350,000 pixels at rate of 30 FPS)
- CD Rom and Internet are too ***SLOW*** to deliver that much data
    - Solution: Reduce resolution (or display size) which will reduce the number of pixels to output
- [Back to Digital Video Quality](#digital-video-quality)

### Frame Rate
- Number of individual video frames (or images) displayed per second
- Standard frame rate for broadcast video is 30 Frames Per Second (FPS)
- Reducing the frame rate reduces the data to be transferred
- Videos on the Internet is often deivered at **15fps**
    - ***WHY?*** -> 15 fps is the threshold for a smooth motion video
- Lowering frame rate will 
    - Slow delivery of individual images (I don't understand but might as well just include)
    - Drop out frames of video
    - Result in "jerky"(or laggy) motion
- [Back to Digital Video Quality](#digital-video-quality)

### Compression method
- Algorithms used to compress and decompress the video
- Compression is ***KEY*** to successful delivery of digital video
- Compression method are chosen based on
    - Output destination
        - DVD
        - Internet
        - Mobile Device
    - Editing capability
        - Detailed editing tasks 
        - Limited editing tasks
    - Type of images in video
        - Complex scenes
        - Similar scenes

#### Three strategies for compressing video
- Intra-frame
    - Re-encodes within the frame
    - ***LOSSLESS*** strategy: RLE
        - RLE -> Run-Length Encoding
        - Results in smaller and more efficient file with all the original data
    - ***LOSSY*** strategy: M-JPEG
        - M-JPEG -> Motion JPEG
        - Individual images are compressed and linked together as motion sequences
        - Best for video editing as every frame is preserved despite data being lost from each separate frame
    - M-JPEG 2000
        - Successor to M-JPEG
        - Preserves intra-frame advantages and scalability
- Inter-frame
    - Eliminates intervening (intermediary) frames and saves only the changes between the frames
    - Known strategy: MPEG compression
    - MPEG compression:
        - (A bit confusing for I-frames and Intra frames, seems like they are sorta connected)
        - [Intraframes VS Interframes](https://www.youtube.com/watch?v=ss8Re56zozY)
        - I-frames (Intra frames): Complete compressed frames
        - P-frames (Predictive Frames): Records significant changes
        - B-frames (Bidirectional frames): Records smaller changes between the I-frame and P-Frames (some use B-frames some don't)
        - So it's like it will take the compressed using Intraframes, and look down to the future frames, identifying what's changing and what's not, and take advantage of that to reduce the file size
    - Decoding MPEG
        - Processor reassembles dropped frames by using I-Frames as a reference to recreate the intervening frames with the changes stored in P-frames and B-frames
    - Good for distributing video
    - Not good for recording and editing video
- Variable bit rate (VBR)
    - VBR assigns more bits to complex scenes and fewer bits to simpler scenes
    - Common option in video editing softwares
    - CBR (Constant bit rate)
        - Assigns same number of bits per second to all parts of the video
- [Back to Digital Video Quality](#digital-video-quality)

# Common Video Codes
- MPEG
    - MPEG-1 -> short videos on Video CD
    - MPEG-4 -> Videos over the web
- MJPEG
    - Less compressed higher quality files without the loss suffered from interframe compression
- RealVideo
    - Proprietary codex for straming video on the Web
- Flash Video
    - (Once) Popular Internet video standard
- QuickTime
    - Cross-platform format supporting variety of codecs and screen resolutions
- Windows Media Video
    - Highly compressed streaming video format from Microsoft
- SDTV
    - Digital format that uses roughly the same resolution as analog TV
- HDTV
    - Uses 16:9 aspect ratio and progressing scanning
- AVCHD
    - A variant of MPEG-4 compression recording at 1080i, 1080p or 720p
- MJPEG 2000
    - Produces smaller files at hiher quality
    - Uses Intra-frame compression
    - Visually lossless
    - Can be lossy or mathematically lossless compression

# Sources of Digital Video 

[//]: # (Stopped at page 15)