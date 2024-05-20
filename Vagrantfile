
Vagrant.configure("2") do |config|
  
  #Configuración de la box de ubuntu
  config.vm.box = "ubuntu/xenial64"
  config.vm.hostname ="examen-jorge"

  

  
   config.vm.provision "shell", inline: <<-SHELL
   #Actualizar paquetes
   #sudo apt update
   #Instalar mysql
   #sudo apt-get install -y mysql-server
   #Generar datos_menu e insertar valores
    echo "-- Insertar datos de ejemplo en la tabla 'menu'" > /home/vagrant/datos_menu.sql
    echo "INSERT INTO gestion_restaurante.menu(idPlato, nombre, descripcion, precio, categoria ) VALUES" >> /home/vagrant/datos_menu.sql
    echo "(1, 'fabada', 'Fabada típica asturiana', 15, 'Primer plato')," >> /home/vagrant/datos_menu.sql   
    echo "(2, 'cachopo', 'Cachopo releno de jamón y queso', 20, 'Segundo plato')," >> /home/vagrant/datos_menu.sql   
    echo "(3, 'Arroz con leche', 'Arroz con leche requemado', 6, 'Postre')" >> /home/vagrant/datos_menu.sql   
   SHELL
end
