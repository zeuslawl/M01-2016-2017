# 1. Tallafocs
        **Què es un sistema tallafocs? Quina és la seva finalitat?**
        
        Es una parte de un sistema o una red que está diseñada para bloquear el acceso no autorizado, permitiendo al mismo tiempo comunicaciones autorizadas.
        
        **Quines generacions de tallafocs hi ha hagut i què millorava cadascun?**
        
        Tres generaciones:
        Primera generación - cortafuegos de red: filtrado de paquetes
        Segunda generación- cortafuegos de estado
        Tercera generación- cortafuegos de aplicación
        
        
       **Quines capes té el model OSI?**
        
        7 Aplicación
        6 Presentación
        5 Sesión 
        4 Transporte
        3 Red
        2 Enlace
        1 Fisico
        
        **Quines capes té el model TCP/IP? En aquest cas feu una breu descripció de les funcionalitats de cada capa.**
        
        Aplicación
        Transport --> Tcp/udp
        Internet --> Ip
        Acceso a red --> Etha. wireless
        
        **A quina capa/capes sol treballar tradicionalment un tallafocs?**
        
        En la capa sesión y transporte.
        
# 2.Tallafocs Linux
        **Busqueu quins són els tradicionals sistemes de tallafocs incorporats en linux i anomeneu-los**
        --iptables--
        Chain input
        chain forward 
        chain output
        
        
        **Quins dels anteriors tallafocs estan instal.lats al fedora de classe? Com ho comproveu?**
        
        iptables -L y debería devolver 3 lineas                diciendo que no hay reglas activas. 
        
        **Algun dels anteriors tallafocs es troba activat?**
        No
        
        **Instal.leu el servidor web httpd o nginx i activeu-ne el servei (dnf installl ...  ; systemctl ....). Indiqueu les comandes i comproveu que des d'una altra màquina podeu accedir via web a la vostra IP (digueu-li a           un       company). Hauria de sortir la plana per defecte.**
        
        dnf install nginx
        systemctl start nginx
        systemctl status nginx --> Para comprobar si esta encendido.
        
        **Activeu el servei firewalld. Indiqueu com ho feu.**
        systemctl start frewalld
        
        **Comproveu si ara es pot seguir accedint.**
        
        El compañero Pau ha intentado acceder y no puede. Si desactivo el firewalld puede acceder.
        
        
# 3.Win7
        **Porta aquest SO algun tallafocs incorporat?**
        
        Si lleva una instalado por defecto.
        
        **Arrenqueu una màquina win7 a isard.escoladeltreball.org**
        
        **Indiqueu com arribar al tallafocs (passos i pantalles)**
        Inicio - Panel de control - sistema y seguridad- Firewall de windows.
        
        **Es troba activat en aquest windows?**
        
        Si se encuentra activado.
        
        **Busqueu un altre tallafocs per windows. Indiqueu la plana web i les prestacions que ens dona. Intenteu que NOMÉS            sigui tallafocs.**
        
       TinyWall. Sólo necesita un megabyte de tu disco duro y funciona como un programa independiente, así que si no tienes mucho espacio disponible es la solución ideal.

       Es también una elección excelente si no quieres gestionar la aplicación constantemente: no hay pop-ups de aviso y       funciona en segundo plano sin agobiar al usuario. En cuanto a sus opciones, cuenta con una lista blanca, listas de bloqueos por puerto y dominios, restricción de acceso de las aplicaciones, soporte IPv6, bloqueos por contraseña y mucho más.

