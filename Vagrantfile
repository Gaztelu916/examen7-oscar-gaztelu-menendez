
Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.50.55"
  config.vm.hostname ="oscar-gaztelu"
  config.vm.synced_folder "." , "/examen7-oscar-gaztelu"

  config.vm.provision "shell", inline: <<-SHELL

 
echo "-- Insertar datos en la tabla 'platos'" > /home/vagrant/datos_menu.sql
echo "INSERT INTO datos_menu.plato(idplato, nombre, descripcion, precio, categoria) VALUES" >> /home/vagrant/datos_menu.sql
echo "('1', 'macarrones', 'pasta italiana', 13.00, 'pasta')," >> /home/vagrant/datos_menu.sql
echo "('2', 'salmon', 'pescado fresco de asturias', 18.00, 'pescados')," >> /home/vagrant/datos_menu.sql
echo "('3', 'cachopo', 'pplato tradicional', 21.00, 'carnes')" >> /home/vagrant/datos_menu.sql
SHELL

end
