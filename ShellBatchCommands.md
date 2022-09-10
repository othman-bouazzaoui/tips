## How to Kill a procces by port number in windows 
> 1 - netstat -ano | findstr :8083 ==> will return PID_NUMBER <br>
> 2 - taskkill /PID PID_NUMBER  /f ==> Juste replace PID_NUMBER by result of first command.