# challenge5

Nama: Putu Ardanatha Pratama

1. "Sein dan Stark port 443 hanya dapat diakses oleh Fern, Flamme, Linie, Lugner"

- **Answer**
  - **Sein port 443** 
  ![image](img/sein1.png)
  ![image](img/denken1-2.png)
  ![image](img/fern1-2.png)
  ![image](img/flamme1-2.png)
  ![image](img/linie1-2.png)
  ![image](img/lugner1-2.png)
  - **Stark port 443**
  ![image](img/stark1.png)
  ![image](img/denken1-1.png)
  ![image](img/fern1-1.png)
  ![image](img/flamme1-1.png)
  ![image](img/linie1-1.png)
  ![image](img/lugner1-1.png)

- **Configuration**
  ```
    iptables -A INPUT -p tcp --dport  443  --source 10.10.10.19 -j ACCEPT
    iptables -A INPUT -p tcp --dport  443 --source 10.10.10.20  -j ACCEPT
    iptables -A INPUT -p tcp --dport  443 --source 10.10.10.28  -j ACCEPT
    iptables -A INPUT -p tcp --dport  443  --source 10.10.10.27 -j ACCEPT
    iptables -A INPUT -p tcp --dport 443 -j DROP
  ```

2. "Sein port 80 hanya bisa diakses oleh Fern dan Flamme"
  - **Sein port 80** 
    ![image](img/sein2.png)
    ![image](img/denken2-2.png)
    ![image](img/fern2-2.png)
    ![image](img/flamme2-2.png)
    ![image](img/linie2-2.png)
    ![image](img/lugner2-2.png)
  - **Configuration**
    ```
      iptables -A INPUT -p tcp --dport  80  --source 10.10.10.28 -j ACCEPT
      iptables -A INPUT -p tcp --dport  80 --source 10.10.10.27  -j ACCEPT
      iptables -A INPUT -p tcp --dport 80 -j DROP
    ```

3. "Stark port 80 hanya bisa diakses oleh Linie dan Lugner"
   - **Stark port 80**
     ![image](img/stark2.png)
     ![image](img/denken2-1.png)
     ![image](img/fern2-1.png)
     ![image](img/flamme2-1.png)
     ![image](img/linie2-1.png)
     ![image](img/lugner2-1.png)

4. "Sein port 443 hanya bisa diakses oleh Denken pada pukul 07.00 - 12.00 dan Stark port 443 hanya bisa diakses oleh Denken pada pukul 13.00 - 18.00"
   - **Stark**
     ![image](img/stark3.png)
     ![image](img/denken3-2.png)
   - **Sein**
     ![image](img/sein3.png)
     ![image](img/denken3-1.png)
