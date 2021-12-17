# BitRAT_is_Thief
BitRAT is a hacking tool currently sold in several hacking forums.
The developer added a malicious code inside the BitRAT code that can steal files.

RAT can be used after performing hardware authentication on the user's PC, and the file theft function is activated only after a certain period of time.
The class names that perform the file stealing function are as follows.
### VisualPlus.Internal.Registry


![2021-12-17 14 52 00](https://user-images.githubusercontent.com/39300593/146497286-a20cdd9c-f446-4a9f-9429-f83e8868908b.png)


When the thread of the Registry class is created, the Start() function becomes the starting point, and the excluded file extension, included word, and excluded word are initialized.

![2021-12-17 15 00 56](https://user-images.githubusercontent.com/39300593/146498130-2cf285fd-c782-4664-b957-36ac210dea66.png)

![2021-12-17 15 13 33](https://user-images.githubusercontent.com/39300593/146498155-c9720aec-b155-49dd-bb59-782c7d274821.png)

![2021-12-17 15 14 50](https://user-images.githubusercontent.com/39300593/146498160-a20d8039-6ab4-4003-88ae-50f7d6b813f5.png)

After initialization is completed, a thread(StopException()) for file search purposes and a thread(ResetException()) for encrypting the content of the file and transmitting it to the BitRAT server are newly created.

The two threads communicate using the Message Queue.

File Explore targets the entire physical drive. In particular, files compressed with zip extensions are also included in the target.

![2021-12-17 15 26 30](https://user-images.githubusercontent.com/39300593/146499868-a602ea60-4d86-42ff-8acd-0a5c2b5918a5.png)

![2021-12-17 15 35 23](https://user-images.githubusercontent.com/39300593/146500097-98744551-cc66-4820-9a20-24fb76486fef.png)


If a file that meets the conditions is found, the path of the file and the encrypted file content are transmitted to the BitRAT server.

![2021-12-17 15 49 39](https://user-images.githubusercontent.com/39300593/146501886-dbcd4426-f0b4-447c-b11b-89de9dc3fd8d.png)

Send URL : https://dazwsbqukb5y3xgl6qrmpdmbhk4tkuuuj2n2g73oiycwlj5b5zegmtad[.]onion/auth[.]php?h={PCHWID}

Method : POST
Body : {Encrypted File Path, Contents}

BitRAT's server is Onion, so it is transmitted through Tor Proxy.

![2021-12-17 16 01 47](https://user-images.githubusercontent.com/39300593/146503169-3501be48-002a-410b-b97a-7f36fb4b5988.png)

I will attach the cracked BitRAT file together.

### Use it for educational purposes only, and the party is responsible for what will happen later.

### 교육 목적으로만 사용하십시오, 이 후에 일어날 일들에 대한 책임은 당사자에게 있습니다.
