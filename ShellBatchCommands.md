## How to Kill a procces by port number in windows 
> 1 - netstat -ano | findstr :8083 ==> will return PID_NUMBER <br>
> 2 - taskkill /PID PID_NUMBER  /f ==> Juste replace PID_NUMBER by result of first command.

## How to get/convert text from/to base64 using git bash
- Convert text to base64 (encode).
> echo -n "text to encode" | base64

- Get base64 text from ecoding text (decoding)
> echo "dGV4dCB0byBlbmNvZGU=" | base64 -d