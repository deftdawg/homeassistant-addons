# "image": "linuxserver/snapdrop:latest"
# inkscape -w 128 -h 128 snapdrop.svg -o icon.png
# "C:\Program Files\Inkscape\bin\inkscape" -w 128 -h 128 snapdrop.svg -o icon.png

FROM linuxserver/snapdrop:latest

# We must patch until this pull request is merged upstream: https://github.com/RobinLinus/snapdrop/pull/288
RUN sed -i "s#const url = protocol + '://' + location.host + '/server' + webrtc;#const url = protocol + '://' + location.host + location.pathname + '/server' + webrtc;#" /app/snapdrop/client/scripts/network.js