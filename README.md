# JGIS

Proyecto de generación de un GIS, funcional y generico que permita almacenar, editar y eliminar elementos dibujados en un mapa.
Dichos elementos seran dinámicos y se podrán generar desde una interface de administracion, pudiedo elegir para cada elemento, color, nombre, icono, y los campos de información relativos al mismo, por ejemplo:
  -Elemento Farola con las propiedades icono, color etc.., con los campos luminarias, estado, año de construccion, ultima revision,etc..
  
# Modelo de datos:
  - Tabla "users" {id,username,password}
  - Tabla "roles" {id,rol_name, user_creation, create_date}
  - Tabla "users_rol" {id_rol,id_user}
  - Tabla "element_type" {id, name, icon, type, color, allow_edit, allow_click, allow_drag, user_creation, user_edit, create_date, edit_date}
  - Tabla "element_fields" {id, id_element_type, name, type, posible_values, user_creation, user_edit, create_date, edit_date}
  - Tabla "element_security" {id_element,id_allow_rol}
  - Tabla "element" {id, id_element_type, lat, log, user_creation, user_edit, create_date, edit_date}
  - Tabla "element_values" {id, id_element, id_field, value, user_creation, user_edit, create_date, edit_date}
