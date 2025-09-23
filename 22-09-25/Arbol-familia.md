# Definición del Árbol Genealógico en Lisp

```lisp
;; Definición de parámetros para el árbol genealógico
(defparameter *Arbol-familiar* 
  '((abuelos
     (masculino 
      (nombre "Luis Martinez")
      (nacimiento 1940)
      (profesion "Carpintero"))
     (femenino 
      (nombre "Maria Gonzalez") 
      (nacimiento 1943)
      (profesion "Maestra")))
    
    (padres
     (masculino
      (nombre "Carlos Martinez")
      (nacimiento 1965)
      (profesion "Ingeniero")
      (padre "Luis Martinez")
      (madre "Maria Gonzalez"))
     (femenino
      (nombre "Ana Lopez")
      (nacimiento 1968) 
      (profesion "Doctora")
      (padre "Pedro Lopez")
      (madre "Carmen Ruiz")))
    
    (hijos
     (masculino
      (nombre "Diego Martinez Lopez")
      (nacimiento 1995)
      (profesion "Estudiante")
      (padre "Carlos Martinez")
      (madre "Ana Lopez"))
     (femenino
      (nombre "Sofia Martinez Lopez")
      (nacimiento 1998)
      (profesion "Estudiante")
      (padre "Carlos Martinez") 
      (madre "Ana Lopez"))
     (masculino
      (nombre "Mateo Martinez Lopez")
      (nacimiento 2001)
      (profesion "Estudiante")
      (padre "Carlos Martinez")
      (madre "Ana Lopez")))))
```