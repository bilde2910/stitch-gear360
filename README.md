# stitch-gear360
Stitching tool for 360° videos captured by the Samsung Gear 360 (SM-C200)

## Usage

    ./stitch-gear360.sh [options] input1 input2 ... output

### Options

    -a, --refine-alignment  Enable alignment refinement.
    -f, --force             Bypass input filename validation.
    -h, --help              Print this help page and exit.
    -l, --compensate-light  Enable light compensation.

Valid input files are one or more .mp4 videos in 3840x1920 resolution from the
SM-C200. Other 360° cameras including the Gear 360 (2017), and other video
resolutions from the SM-C200, are not supported. Passing other input videos to
this program will result in an error. Note that if you have renamed your 360°
video file, it will be treated as an invalid input file. In such cases, you can
force this program to load the file anyway using --force.

If multiple input videos are specified, they will be joined together to one
long output file.

The output file must be an .mp4 file.

## Dependencies

- ncurses
- ffmpeg
- bash
- [fisheyeStitcher](https://github.com/drNoob13/fisheyeStitcher)
- [spatial-media tools](https://github.com/google/spatial-media/)
- [grid_xd_yd_3840x1920.yml.gz](https://github.com/drNoob13/fisheyeStitcher/blob/master/utils/grid_xd_yd_3840x1920.yml.gz) located within `/usr/share/fisheye-stitcher`

## Thanks

Thanks a lot to drNoob13 for his project fisheyeStitcher. This script is merely a wrapper around that project.
