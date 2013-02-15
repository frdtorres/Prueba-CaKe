<html>  

    <h2><center><?php  echo 'PROYECTO DE VISTA DE TAREAS'; ?></h2></center>
        <?php if(empty($tarea)) ?>
               No hay tareas en esta lista
        <!--<?php //else ?> -->     
        <table border=1>
               <tr><th>Título</th>
                   <th>Estatus</th>
                   <th>Creado</th>
                   <th>Modificado</th>
                   <th>Acciones</th>
               </tr> 
        <?php foreach ($tareas as $tarea): ?>
               <tr><td> <?php echo $this->tarea['Tarea']['titulo'] ?></td>
                   <td> <?php if($tarea['Tarea']['hecha'])
                              echo "Hecha";
                              else echo "Pendiente";?> 
                    </td>
                    <td> <?php echo $this->tarea['Tarea']['created'] ?></td>
                    <td> <?php echo $this->tarea['Tarea']['modified'] ?></td>
                    <td> <?php echo $this->Html->link('Editar', array('action'=>'edit', $tarea['Tarea']['id'])); ?> </td>
                </tr>
            <?php endforeach; ?> 
        </table> 
        <!--<?php //endif; ?>-->
        <?php echo $this->Html->link('Añadir Tarea',array('action'=>'add')); ?>
  
</html>
