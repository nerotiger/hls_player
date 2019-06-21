# hls_player
http live streaming

run on http server,

it won't work with file:// directly, for some ajax cross-domain issue.

<i>
Access to XMLHttpRequest at '.m3u8' from origin 'null' has been blocked by CORS policy: 
Cross origin requests are only supported for protocol schemes: http, data, chrome, chrome-extension, https.
</i>
<br />
<b>
  to generate TS segments
</b>
<br />
<code>
  ffmpeg -i input.mp4 -hls_time 10 -hls_list_size 0 -bsf:v h264_mp4toannexb -hls_segment_filename 'o_%03d.ts' out.m3u8
</code>
