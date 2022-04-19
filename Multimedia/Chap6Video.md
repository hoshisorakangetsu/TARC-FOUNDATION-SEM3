# Video

### Video can be perceived as ***MOVING PICTURES***
- Much like animation, videos or films are a series of rapidly displaying pictures
- Each picture captures an instance of a motion
- ***PERSISTENCE OF VISION*** helps in perception of flow of motion.

# Table of Contents
1. [Analog](#analog)
2. [Digital Video](#digital-video)
    - [Quality](#digital-video-quality)
    - [Compression](#compression-method)
3. [Video Codecs](#common-video-codecs)
4. [Source of Digital Video](#sources-of-digital-video)
5. [Original Digital Video](#original-digital-video)
    - [Shooting](#shooting)
    - [Editing](#editing)
    - [Rendering](#rendering)
6. [Guidelines](#guidelines-for-video)

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

# Common Video Codecs
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
- Convert existing analog to digital
- Create or purchase digital footage

# Original Digital Video

### Steps
- [Shooting](#shooting)
- [Editing](#editing)
- [Rendering](#rendering)

# Shooting
- Requires planning for
    - Intended uses of video
    - List of shots required
    - Weather and lighting conditions
    - Availability of personnel
    - How the video will be integrated (used) in the project
- Shooting to Record
    - Captures ultimate form of video as shooting is done
    - No editing is applied later
    - Used to capture event and immediately share with others
- Shooting to Edit
    - Captures source video with editing in mind
    - Shoots a variety of video clips that will later be edited (like trimmed, re-ordered or blended) into a single video

### Digital Video Camera Considerations
- CCD (Charge-Coupled Device)
    - Generates levels of electric voltage based on the variation of light intensity striking the surface
    - Converts voltages to digital values to store data about each pixel in the image
    - Size varies from 1/16 to 1/2 inch
    - Larger CCDs are more expensive
- Number of CCDs
    - One single CCD: Light is filtered and level of each filtered color is recorded
    - Three CCDs: Light is split in to three channels (Red Green Blue) and each CCDs records the separate levels of the RGB
        - Clearer and more accurate color
- Resolution of CCD
    - Higher resolution = More accurate images
    - Let motion capture math the resolution to the format (I no understand)
    - Camera selection should always based on resoltuion of CCD, not digital enlargement ratings
- Lens
    - Look for high quality lens from better vendors
    - Ignore software zoom capabilities
- Light sensitivity
    - Lower ***LUX*** ratings indicates the camera can operate in lower light conditions
        - LUX(lx) -> SI unit for illuminance
    - DV camcorders vary from 2 to 8 lux
    - Supplemental lighting may be needed for dimly lit conditions
- Microphones
    - Omni-directional: Optimized for broad range of background sound
    - Unidirectional: Record from narrowly defined location
    - Placement on handle toward front of camera is preferred to avoid the sound coming from the camera itself
    - Headphones give direct feedback of microphone effectiveness
- Storage Media
    - Tape
        - Advantages
            - Inexpensive archive format
            - DV and HDV formats are well established
        - Disadvantages
            - Sequential access demanding
            - Transfer of video to another device is time consuming
    - Optical Media & Solid State Media (BIAS EH ALL IN NOTES IS ADVANTAGES NIA)
        - Random access to video
        - Rapid transfer from camera to another device
        - Light weight
        - Low power consumption
        - Ease of exchange and transport
        - Lower cost
        - Increased capacities
- File format
    - Source video footage should be captured at highest resolution possible and not be highly compressed (for editing capabilities and High res sharing)
    - DV Format
        - Limits compression to 5:1
        - Relatively high resolution
        - Uses M-JPEG compression
    - HD & 3D Format
        - New formats lai
        - HD formats increase processor demand during editing if using inter-frame compression

### Shooting basics
- Framing a shot
    - Rule of thirds
        - Widely embraced guideline for framing a video shot
        - Preserves its interest
        - Meaningfully relates it to action taking place
        - Ensures adequate side and headroom
- Minimize camera motion
    - Use a tripod or a steady surface to support the camera
    - Keep the camera still
- Camera controls to generate motion
    - Pan: Move camera side-to-side
    - Zoom: Enlarge with the camera lens
- Take care of time code
    - Format: hours, minutes, seconds, frames
    - Timecode will become the frame's address when accessing it
    - Editing softwares uses time code for splits, trims and transitions
    - Camera will record the code but
        - Code can be lost if the user shifts to VCR mode to view video and advances to new location to continue shooting
        - Look for camera's ***"End Search"*** control to restart the code
    - Less important if optical & solid state recording formats are used
- Get the right shots
    - Source video needs to cover all the important elements of the subject
    - Variety of shot techniques can be used to tell the story
        - Close up shot (CU)
        - Medium shot (MS)
        - Wide shot (WS)
        - Establishing shot
        - Cutaway
        - Point of view shot
        - Reverse angle shot
        - Over the shoulder shot

[Back to Steps](#steps)

# Editing
- Software Options
    - Consumer packages
    - Prosumer applications (Prosumer is whom produces and consumes)
    - Specialized video and film production
- Features
    - Capture video from external source
    - Arrange separate video clips
    - Split and trim clips
    - Add transition and special effects

### Capture / Importing Video
- Transfer video from camera to computer through USB, FireWire or Thunderbolt connection
- Transfers include
    - Video images & audio
    - Time code
    - Date stamp
    - Scene Detection
    - Geotagging
- Editing can use the changes in data to identify different recording sessions

### Batch capture
- Transfer only a selected portions of a source tape
    - Portions are pre-selected by "in" and "out" points
- Editing software transfers only the marked video scenes to the computer's hard drive
- Clips are labeled with names and time codes in a library window

### Basic Video Editing
- Captured clips are used as the ***SOURCE VIDEO*** to create the finished product
- Source video clips are arranged on a construction window
    - The clip is now a part of the ***MASTER VIDEO***
        - Master Video 
            - the segments being developed in the editing environment
            - A series of instructions and pointers for performing operations on the original source footage
- Editing software
- ![KDENLIVE](./imgRes/mtm_c5_kdenlive.jpg)
    - Library Window
        - Clips transferred to the computer
    - Preview Window
        - Source Video
    - Construction Window
        - Assembled clips (or master video)
    - Timeline
        - Duration of video's multiple tracks
- Editing Operations
    - Splitting
        - Divides clips into multiple parts
    - Trimming
        - Removes unwanted frames from the clips
    - Transitions
        - Special effects to move into or out of a clip
            - Cut
            - Fades
            - Dissolve
            - Wipe

[Back to Steps](#steps)

# Rendering
- Process of applying all the editing operations specified in the master video to produce a new independent video file
- A processor intensive and time consuming process
- Output options should base on video's intended use
    - Output options:
        - Video compression method
        - Resolution (screen size)
        - Frame rate and video data rate
        - Audio data rate and audio format

### Rendering Decisions
- Choice of a codec
    - Videos must be compressed
    - Choice determines the quality of the resulting video
        - VBR can be better than CBR
- Choice of screen resolution
    - Depends on mode of delivery
        - DVD: 720x480
        - CD: 320x240
        - Web: 240x180
        - Cell Phones: 176x144
- Choice of frame rate
    - Impacts size of video file
    - Web video should be significantly reduced for a wide viewing audience
- Choice of video data rate
    - Low quality web video: 20 - 30 KB/s
    - Typically set in codec software preferences
    - DVD high quality video: 9MB/s
    - Blu-ray disc: 48 MB/s
- Choice of audio compression and data rate
    - If file size is not critical, use PCM format
        - PCM -> Pulse-Code Modulation
            - A method used to digitally represent sampled analog signals
    - Well-known alternatives:
        - MP3
        - Dolby Digital AC-3
- Choice of computer hardware
    - The complexity of video can make render time over 1 hour for 1 minute of video
    - CPU speed, amount of RAM, size of hard drive can save time
        - Multi-core processors and distributed processing can also reduce the time for rendering
        - Now got GPU rendering technology d

[Back to Steps](#steps)

# Guidelines for Video
- Shooting
    - Choose camera carefully
    - Steady the camera
    - White balance prior to shooting
    - Avoid shooting into light and backlit scenes
    - Limit the number of pans and zooms
    - Frame the subject
        - Popular way: Rules of Third
    - Make inventory of required shots
    - Use highest resolution possible
    - Add external microphones
    - Use headphones to monitor sound quality
    - Record background sound for use in editing
    - Don't break the time code
- Editing
    - Protect source video
    - Save a copy of the master video before rendering
- Rendering
    - Match for intended use and delivery medium:
        - Codec
        - Resolution
        - Frame rate
        - data rate
    - Use VBR encoding when available
