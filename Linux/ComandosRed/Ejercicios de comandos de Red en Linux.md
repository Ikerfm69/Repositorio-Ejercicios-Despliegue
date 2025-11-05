# Ejercicios de comandos de Red en Linux



[TOC]

## Ejercicios

1. **Muestra todas las interfaces de red activas y sus direcciones IP en el sistema.**

   ```bash
   $ ip addr show
   ```

   ![image-20251105111315354](./Ejercicios comandos de red Linux.assets/image-20251105111315354.png)

2. **¿Cómo mostrarías solo la información de la interfaz de red `eth0` usando `ip a`?**

   ```bash
   $ ip addr show dev enp0s3
   ```

   ![image-20251105111849408](./Ejercicios comandos de red Linux.assets/image-20251105111849408.png)

3. **Configura manualmente la dirección IP `192.168.1.100/24` en la interfaz `eth0` con `ifconfig`.**

   ```bash
   sudo ifconfig eth0 192.168.1.100 netmask 255.255.255.0 up
   ```

   ![image-20251105112128194](./Ejercicios de comandos de Red en Linux.assets/image-20251105112128194.png)

4. **Envía 10 paquetes ICMP a la dirección IP `8.8.8.8` usando `ping`.**

   ```bash
   $ sudo ping -c 10 8.8.8.8
   ```

   ![image-20251105112719686](./Ejercicios de comandos de Red en Linux.assets/image-20251105112719686.png)

5. **Consulta la dirección IP de `www.example.com` usando `nslookup`.**

   ```bash
   $ nslookup www.example.com
   ```

   ![image-20251105112846875](./Ejercicios de comandos de Red en Linux.assets/image-20251105112846875.png)

6. **Muestra las conexiones TCP activas en el sistema usando `netstat`.**

   ```bash
   $ sudo netstat -tp
   ```

   ![image-20251105112941705](./Ejercicios de comandos de Red en Linux.assets/image-20251105112941705.png)

7. **Descarga el contenido de la página principal de `www.example.com` usando `curl` y guárdalo en un archivo llamado `example.html`.**

   ```bash
   $ curl -sS https://www.example.com -o example.html
   ```

   ![image-20251105113104182](./Ejercicios de comandos de Red en Linux.assets/image-20251105113104182.png)

8. **Consulta el nombre del host actual del sistema.**

   ```bash
   $ hostname
   ```

   ![image-20251105113126437](./Ejercicios de comandos de Red en Linux.assets/image-20251105113126437.png)

9. **Obtén la información de registro del dominio `example.com` usando `whois`.**

   ```bash
   $ whois example.com
   ```

   ![image-20251105113220174](./Ejercicios de comandos de Red en Linux.assets/image-20251105113220174.png)

10. **Cambia temporalmente el nombre del host a `servidor01` usando `hostname`.**

    ```bash
    $ sudo hostname servidor01
    ```

    ![image-20251105113300237](./Ejercicios de comandos de Red en Linux.assets/image-20251105113300237.png)

11. **Envía un ping a la dirección `192.168.1.1` y muéstralo en modo detallado (verbose).**

    ```bash
    $ ping -v 192.168.1.1
    ```

    ![image-20251105113453370](./Ejercicios de comandos de Red en Linux.assets/image-20251105113453370.png)

12. **Muestra las estadísticas de la red, como la cantidad de paquetes transmitidos, usando `netstat`.**

    ```bash
    $ netstat -s
    ```

    ![image-20251105113513457](./Ejercicios de comandos de Red en Linux.assets/image-20251105113513457.png)

13. **Realiza una consulta inversa para obtener el nombre de dominio asociado a la IP `8.8.8.8` con `nslookup`.**

    ```bash
    $ nslookup 8.8.8.8
    ```

    ![image-20251105113548004](./Ejercicios de comandos de Red en Linux.assets/image-20251105113548004.png)

14. **Configura temporalmente la máscara de subred `255.255.255.128` en la interfaz `eth1` usando `ifconfig`.**

    ```bash
    $ sudo ifconfig enp0s3 192.168.1.130 netmask 255.255.255.128 up
    ```

    ![image-20251105113922599](./Ejercicios de comandos de Red en Linux.assets/image-20251105113922599.png)

15. **Muestra las rutas de enrutamiento actuales usando `netstat`.**

    ```bash
    $ netstat -rn
    ```

    ![image-20251105114003599](./Ejercicios de comandos de Red en Linux.assets/image-20251105114003599.png)

16. **Realiza una solicitud HTTP GET a la API de GitHub para obtener los repositorios de `usuario123` usando `curl`.**

    ```bash
    $ curl -sS https://api.github.com/users/usuario123/repos
    ```

    ![image-20251105114119623](./Ejercicios de comandos de Red en Linux.assets/image-20251105114119623.png)

17. **Envía un ping a la dirección `2001:4860:4860::8888` (IPv6 de Google) con `ping6` y limita los paquetes a 4.**

    ```bash
    $ ping6 -c 4 2001:4860:4860::8888
    ```

    

18. **Obtén las estadísticas de los sockets activos en el sistema con `netstat`.**

    ```bash
    $ netstat -s
    ```

    ![image-20251105115111032](./Ejercicios de comandos de Red en Linux.assets/image-20251105115111032.png)

19. **Cambia temporalmente la dirección MAC de la interfaz `eth0` a `00:11:22:33:44:55` usando `ifconfig`.**

    ```bash
    $ sudo ifconfig eth0 down
    $ sudo ifconfig eth0 hw ether 00:11:22:33:44:55
    $ sudo ifconfig eth0 up
    ```

    ![image-20251105115315636](./Ejercicios de comandos de Red en Linux.assets/image-20251105115315636.png)

20. **Realiza una solicitud HTTP POST a `https://httpbin.org/post` enviando el usuario `admin` y la contraseña `12345` usando `curl`.**

    ```bash
    $ curl -sS -X POST -d "user=admin&password=12345" https://httpbin.org/post
    ```

    ![image-20251105115537586](./Ejercicios de comandos de Red en Linux.assets/image-20251105115537586.png)

21. **Consulta el nombre de dominio completo (FQDN) de tu sistema usando `hostname`.**

    ```bash
    $ hostname -f
    ```

    ![image-20251105115639616](./Ejercicios de comandos de Red en Linux.assets/image-20251105115639616.png)

22. **Muestra solo las conexiones activas en la interfaz `eth0` usando `netstat`.**

    ```bash
    $ ss -tn src 192.168.1.100 or dst 192.168.1.100
    ```

    ![image-20251105115932912](./Ejercicios de comandos de Red en Linux.assets/image-20251105115932912.png)

23. **Muestra las conexiones activas con nombres de dominio en lugar de direcciones IP usando `netstat`.**

    ```bash
    $ netstat -atp
    ```

    ![image-20251105120004634](./Ejercicios de comandos de Red en Linux.assets/image-20251105120004634.png)

24. **Configura una nueva puerta de enlace predeterminada con la dirección `192.168.1.1` usando `ip route`.**

    ```bash
    $ sudo ip route add default via 192.168.1.1 dev eth0
    ```

    

25. **¿Qué comando usarías para ver todas las rutas configuradas en tu sistema?**

    ```bash
    $ ip route show
    ```

    ![image-20251105120152119](./Ejercicios de comandos de Red en Linux.assets/image-20251105120152119.png)

26. **¿Cómo configuras que todo el tráfico destinado a la red `10.10.10.0/24` pase por el gateway `192.168.1.1` en la interfaz `eth0`?**

    ```bash
    $ sudo ip route add 10.10.10.0/24 via 192.168.1.1 dev eth0
    ```

27. **¿Cómo eliminas la ruta añadida en el ejercicio anterior?**

    ```bash
    $ sudo ip route del 10.10.10.0/24 via 192.168.1.1 dev eth0
    ```

28. **Si la interfaz `eth0` está deshabilitada, ¿qué comando usarías para levantarla?**

    ```bash
    $ sudo ip link set enp0s3 up
    ```

29. **¿Qué comando utilizas para asignar la dirección MAC `02:1A:2B:3C:4D:5E` a la interfaz `eth0`?**

    ```bash
    $ sudo ip link set dev eth0 address 02:1A:2B:3C:4D:5E
    ```

    ![image-20251105120608193](./Ejercicios de comandos de Red en Linux.assets/image-20251105120608193.png)

30. **¿Cómo renombrarías la interfaz `eth0` para que pase a llamarse `lan0`?**

    ```bash
    $ sudo ip link set eth0 name lan0
    ```

![image-20251105120811562](./Ejercicios de comandos de Red en Linux.assets/image-20251105120811562.png)