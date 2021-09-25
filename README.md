# Jarkom-Modul-1-IUP7-2021

## Ascarya Arkaandhiyaa Allaam 05111942000027
## Farah Dhiah Qorirah 05111942000018	
## Julius Adetya Eka Bhaswara 05111942000026	


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
