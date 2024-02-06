document.addEventListener('DOMContentLoaded', function() {
  const taskInput = document.getElementById('taskInput');
  const addTaskBtn = document.getElementById('addTaskBtn');
  const taskList = document.getElementById('taskList');
  const title = document.getElementById('title');

  // Función para agregar un pendiente
  function addTask() {
    const taskText = taskInput.value.trim();
    if (taskText !== '') {
      const li = document.createElement('li');
      li.textContent = taskText;

      // Botón de completado
      const completeBtn = document.createElement('button');
      completeBtn.textContent = '✔';
      completeBtn.classList.add('complete');
      completeBtn.addEventListener('click', function() {
        li.classList.toggle('completed');
      });

      // Botón de editar
      const editBtn = document.createElement('button');
      editBtn.textContent = '✎';
      editBtn.classList.add('edit');
      editBtn.addEventListener('click', function() {
        const newText = prompt('Editar pendiente:', li.textContent);
        if (newText !== null) {
          li.textContent = newText;
        }
      });

      // Botón de borrar
      const deleteBtn = document.createElement('button');
      deleteBtn.textContent = '❌';
      deleteBtn.classList.add('delete');
      deleteBtn.addEventListener('click', function() {
        taskList.removeChild(li);
      });

      li.appendChild(completeBtn);
      li.appendChild(editBtn);
      li.appendChild(deleteBtn);

      taskList.appendChild(li);
      taskInput.value = '';
    }
  }

  addTaskBtn.addEventListener('click', addTask);
});
