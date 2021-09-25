# Jarkom-Modul-1-IUP7-2021

## Ascarya Arkaandhiyaa Allaam 05111942000027
## Farah Dhiah Qorirah 05111942000018	
## Julius Adetya Eka Bhaswara 05111942000026	

1.  What web server is used on "ichimarumaru.tech"!
    
    Using display filter:
    
    ```shell
    http.host == ichimarumaru.tech
    ```
    
    [![image.png](https://i.postimg.cc/pVKQ2dLH/image.png)](https://postimg.cc/XX7BL45H)
    
    Then, right click, Follow and and click TCP Stream
    
    [![image.png](https://i.postimg.cc/Z5WC5fxd/image.png)](https://postimg.cc/sMRVn48j)
    
    The server is nginx/1.18.0 (Ubuntu) 

2.  Find the packets from the web that use the basic authentication method!
    
    Using display filter:
    
    ```shell
    http.authbasic
    ```
    
    [![image.png](https://i.postimg.cc/3wgp3S3Z/image.png)](https://postimg.cc/94QzpBR4)
    
3.  Follow the instructions at basic.ichimaru maru.tech! Username and password can be obtained from the .pcapng file!
    
    Using display filter:
    
    ```shell
    http.host == basic.ichimarumaru.tech
    ```
    
    [![image.png](https://i.postimg.cc/15r3RkFX/image.png)](https://postimg.cc/Vd58DHDP)
    
    We can find the username and password is:
    Username: kuncimenujulautan
    Password: tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN
    
    After that, we tried to login to the website with that username and password. After login, theres a question about T568A cable configuration
    
    [![image.png](https://i.postimg.cc/Zqpdcfgd/image.png)](https://postimg.cc/Lq454Vm9)
    
    Then, we answered it with:
    1. White Green 
    2. Green 
    3. White Orange
    4. Blue
    5. White Blue
    6. Orange
    7. White Brown 
    8. Brown
    
    - Problem that we get:

        We tried to export object and download the file with login name:
        
        [![image.png](https://i.postimg.cc/NFw2SR3z/image.png)](https://postimg.cc/7GmLTJY3)
        
        [![image.png](https://i.postimg.cc/rFrYSTjy/image.png)](https://postimg.cc/56f3VZDD)
        
        and we got:
        Username: seijaku
        Password: bukanpasswordnya
        
        [![image.png](https://i.postimg.cc/rwtc0705/image.png)](https://postimg.cc/zy544tkf)

        we cannot login with that username and password

4.  Find the mysql packets that contain the select query command!

    Mysql contains “select” -> To find the mysql packets that contain select query
    
    ![image](https://user-images.githubusercontent.com/77782259/134764962-5774fc5a-a515-4a7c-ad11-3d94f6324e87.png)

5.  Login to portal.ichimarumaru.tech then follow the instructions! The username and password can be obtained from the insert query in the users table from the .pcap file!
    
    ![image](https://user-images.githubusercontent.com/77782259/134764979-e2443dcd-0281-4235-8b90-9434143c475d.png)

    Mysql contains table -> To search the username and password from the table
    
    Then, when we click on follow TCP stream, the contents are likely the screenshot above then save it as .txt file to find the username and password from the insert query sql
    
    ![image](https://user-images.githubusercontent.com/77782259/134765008-476d2163-3db9-4604-953d-0090443310f9.png)

    ![image](https://user-images.githubusercontent.com/77782259/134765016-66f78185-889c-48d9-a913-cb4ad7af32c8.png)
    
    Then we can find the username and password in the .txt file that have been saved before. The username is “akakanomi” and the password is “pemisah4lautan”. After we found the     username and password, we fill the username and password that we have found before into the portal.ichimarumaru.tech then login in. After that follow the instruction that is     displayed on the web
    
    ![image](https://user-images.githubusercontent.com/77782259/134765052-1841fd7a-194b-43c7-a809-17eff9d44bb2.png)
    
6.  Find username and password when logging into FTP Server!

    ftp.request.command == USER || ftp.request.command == PASS -> To find username and password when logging into FTP server. The username is "secretuser" whether the password       is "aku.pengen.pw.aja"
    
    ![image](https://user-images.githubusercontent.com/77782259/134765134-42ab0617-3158-4c16-9d34-06927f9b9556.png)

7.  There are 500 zip files saved to FTP Server with names 0.zip, 1.zip, 2.zip, ..., 499.zip. Save and Open the pdf file. (Hint = the name of the pdf is "Real.pdf")

    Using display filter:
    
    ```shell
    ftp-data and frame contains “Real.pdf”
    ```
    Right click, follow then click TCP Stream
    
    [![image.png](https://i.postimg.cc/1RGZQpxr/image.png)](https://postimg.cc/F1H6bkHY)
    
    [![image.png](https://i.postimg.cc/sXPHt4BB/image.png)](https://postimg.cc/Q9tq75Js)
    
    change show data as Raw, then save the file
    
    [![image.png](https://i.postimg.cc/yN4PsSC0/image.png)](https://postimg.cc/QFm5qCtM)
    
    Then open the file, and yeah, we got rickrolled
    
    [![image.png](https://i.postimg.cc/5NQLyN3g/image.png)](https://postimg.cc/KRFRsbC3)
    
8.  Look for the packets that show the retrieval of files from the FTP!
    
    Using display filter:
    
    ```shell
    ftp.request.command == RETR
    ```
    
    [![image.png](https://i.postimg.cc/cLm7Y1Kn/image.png)](https://postimg.cc/211BND7k)
    
9.  From the packets going to FTP, there are indications of storing some files. One of them is a file containing confidential data with the name "secret.zip". Save and open the file!
    
    Using display filter:
    
    ```shell
    ftp-data.command == "STOR secret.zip"
    ```
    Right click, follow and click TCP Stream
    
    [![image.png](https://i.postimg.cc/x14CBBhZ/image.png)](https://postimg.cc/TKnfDNRj)
    
    [![image.png](https://i.postimg.cc/ydF8gxxq/image.png)](https://postimg.cc/zbGr4JTp)
    
    Change show data as Raw, and save the file
    
    [![image.png](https://i.postimg.cc/nhgF3BQb/image.png)](https://postimg.cc/Bj5f68gM)
    
    Then, we got a zip that need a password to be openned 

    [![image.png](https://i.postimg.cc/QNmjRRWq/image.png)](https://postimg.cc/CdZy8r7Z)

10. Also there is "history.txt" which probably contains the history of the bash server! Use the contents of "history.txt" to find the password to open the secret file in "secret.zip"!
    
    Using display filter:
    
    ```shell
    ftp-data and frame contains "secret.zip"
    ```
    right click, follow then click TCP Stream
    
    [![image.png](https://i.postimg.cc/mgQXnGPL/image.png)](https://postimg.cc/68pf7gVg)
    
    [![image.png](https://i.postimg.cc/4xQC9cbQ/image.png)](https://postimg.cc/WdzfRhyd)
    
    Then i saw theres txt file nammed bukanapaapa.txt. After that i search bukanapaapa.txt using display filter:
    
    ```shell
    ftp-data.command == "STOR bukanapaapa.txt"
    ```
    
    Right click, follow and click TCP Stream
    
    [![image.png](https://i.postimg.cc/YCs68n3r/image.png)](https://postimg.cc/FY0kHx88)
    
    Then we found the password for the zip file from number 9
    
    [![image.png](https://i.postimg.cc/VLH0cSb4/image.png)](https://postimg.cc/YhYC6CRm)
    
    Then we tried to open the wanted.pdf inside secret.zip
    
    [![image.png](https://i.postimg.cc/TPvwRn2j/image.png)](https://postimg.cc/4YwZP79n)
    
    And we found luffy
    
    [![image.png](https://i.postimg.cc/7Z0HQb15/image.png)](https://postimg.cc/qNBHNJ5r)
    
    
11. Picks up packets coming from port = 80

    Using capture filter ‘tcp src port 80’
    
    ![image](https://user-images.githubusercontent.com/73812417/134704773-195b646f-8119-455e-8ec9-28ce0a4cd9a1.png)

12. Picks up packets containing port = 21

    Using capture filter ‘tcp src port 21’
    
    ![image](https://user-images.githubusercontent.com/73812417/134704822-94e68d41-1558-4b10-a4e0-7d1cc7a5cd15.png)

13. Shows packets going to port = 443

    capture file with 'dst port 443'
![13](https://user-images.githubusercontent.com/73812417/134363822-c663f7df-cf4c-41c8-bb60-f51454b213fd.png)


14. Picks up packets going to kemenag.go.id

    We need to open kemenag.go.id website first then capture file with 'dst host kemenag.go.id'
  ![14](https://user-images.githubusercontent.com/73812417/134363164-9e8aa8e9-7a3d-4149-ad5f-67960a4f832c.png)

15. Picks up packets coming from local ip address 

    Get the local ip address by typing ipconfig in command prompt. I get my local ip address is  192.168.100.70, so capture file with 'src host 192.168.100.70'
![15](https://user-images.githubusercontent.com/73812417/134364142-1af856d2-a2f3-42ee-9588-ece058ce4b87.png)
