# MSU Mapping Project

![Object Rotation](./renders/objects/sparty/sparty.gif)

# Data

The data folder has the following structure

```
├── objects
│   ├── object_1
│   │   ├── combined
│   │   ├── video_1
│   │   └── video_2
│   └── object_2
│       ├── combined
│       ├── video_1
│       └── video_2
└── scenes
    ├── scene_1
    │   ├── combined
    │   ├── video_1
    │   └── video_2
    └── scene_2
        ├── combined
        ├── video_1
        └── video_2
```


# Visualizing Objects

To visualize the object rotating render, you can insert the GIF file using the following markdown syntax:

![Object Rotation](./renders/objects/hannah_statue/hannah_statue.gif)

```
$ ffmpeg -i video.mp4 -vf "crop=960:1080:480:0" video_cropped.mp4
$ ffmpeg -i video_cropped.mp4  -vf "palettegen" palette.png
$ ffmpeg -i video_cropped.mp4 -i palette.png -filter_complex "paletteuse" video.gif
```