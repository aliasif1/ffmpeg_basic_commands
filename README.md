# FFMPEG Basic commands 

## convert from raw (.y4m) to mp4 (avc encoder)
`
ffmpeg -i input.y4m output.mp4
`
The encoded video will have crf = 23 (default for avc)

## Extract segments of duration x seconds from raw (.y4m)
`
ffmpeg -i input.y4m -segment_time 00:00:02 -f segment segment%003d.y4m
`
The encoded video will have a duration of 2 seconds (x)

## Get the first x seconds from raw (.y4m)
1 
`
ffmpeg -i input.y4m -vframes fps*x out.y4m

`
2
`
ffmpeg -i input.y4m -ss 00:00:20 -to 00:00:40 out.y4m

`
3
`
ffmpeg -i input.y4m -t 20 out.y4m

`
