# Jarkom-Modul-1-IUP7-2021

## Ascarya Arkaandhiyaa Allaam 05111942000027
## Farah Dhiah Qorirah 05111942000018	
## Julius Adetya Eka Bhaswara 05111942000026	


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
