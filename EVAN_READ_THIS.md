Seems like this project doesn't play well with either MacOS Catalina or with McAfee on Mac.

Do the following to run on windows:
1. Ensure Node.js is installed (>v8.0)
1. Download [youtube-dl](https://ytdl-org.github.io/youtube-dl/download.html) and run `youtube-dl.exe`
1. Download and extract [ffmpeg](https://ffmpeg.zeranoe.com/builds/)
    1. After extracting, rename the extracted folder to `ffmpeg` or something more manageable
1. Ensure youtube-dl and ffmpeg have been added to PATH
    1. If one or both are not present in `PATH`, open a command prompt window with adminstrator privileges and run the following command to add a command to `PATH`:    
        ```
        setx /M APTH "%PATH%;C:\<Path_to_folder>\ffmpeg\bin"
        ```
1. Run `echo %PATH%` to confirm a command has been added to `PATH`

-----

Now everything should work fine and you can follow the project README to run
1. Edit `destreamer.ts` and replace:
    1. `username` with `<userId>@company.net`
    1. `outputDirectory` with `C:/Users/<userId>/Github`
1. Run `npm install`
1. Run `npm start <Microsoft_Stream_Video_URL>`
