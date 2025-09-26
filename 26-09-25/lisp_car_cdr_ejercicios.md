# Ejercicios de Lisp - Problemas con car y cdr

## Soluciones a los ejercicios

### 1. Lista: (a b c d e) → Extraer d
```lisp
(car (cdr (cdr (cdr '(a b c d e)))))
; o alternativamente:
(cadddr '(a b c d e))
```

### 2. Lista: ((1 2) (3 4) (5 6)) → Extraer 5
```lisp
(car (car (cdr (cdr '((1 2) (3 4) (5 6))))))
; o alternativamente:
(caar (cddr '((1 2) (3 4) (5 6))))
```

### 3. Lista: ((a b) (c d) (e f)) → Extraer e
```lisp
(car (car (cdr (cdr '((a b) (c d) (e f))))))
; o alternativamente:
(caar (cddr '((a b) (c d) (e f))))
```

### 4. Lista: ((x y) ((p q) (r s)) (z w)) → Extraer z
```lisp
(car (car (cdr (cdr '((x y) ((p q) (r s)) (z w))))))
; o alternativamente:
(caar (cddr '((x y) ((p q) (r s)) (z w))))
```

### 5. Lista: ((1 (2 3)) (4 (5 6))) → Extraer 6
```lisp
(car (cdr (car (cdr (car (cdr '((1 (2 3)) (4 (5 6)))))))))
; o alternativamente:
(cadr (cadr (cadr '((1 (2 3)) (4 (5 6))))))
```

### 6. Lista: (((a b) c) d e) → Extraer c
```lisp
(car (cdr (car '(((a b) c) d e))))
; o alternativamente:
(cadar '(((a b) c) d e))
```

### 7. Lista: ((1 2) 3) ((4 5) 6)) → Extraer 6
```lisp
(car (cdr (car (cdr '(((1 2) 3) ((4 5) 6))))))
; o alternativamente:
(cadar (cdr '(((1 2) 3) ((4 5) 6))))
```

### 8. Lista: ((p (q (r s))) t u) → Extraer (r s)
```lisp
(car (cdr (car (cdr (car '((p (q (r s))) t u))))))
; o alternativamente:
(cadar (car '((p (q (r s))) t u)))
```

### 9. Lista: (((a) b) (c (d e)) f) → Extraer d
```lisp
(car (car (cdr (car (cdr '(((a) b) (c (d e)) f))))))
; o alternativamente:
(caar (cdr (cadr '(((a) b) (c (d e)) f))))
```

### 10. Lista: ((1 (2 (3 4))) (5 6)) → Extraer 3
```lisp
(car (car (cdr (car (cdr (car '((1 (2 (3 4))) (5 6))))))))
; o alternativamente:
(caar (cdr (cadr (car '((1 (2 (3 4))) (5 6))))))
```

### 11. Lista: (((x) (y)) ((z) (w))) → Extraer (w)
```lisp
(car (cdr (car (cdr '(((x) (y)) ((z) (w)))))))
; o alternativamente:
(cadr (cadr '(((x) (y)) ((z) (w)))))
```

### 12. Lista: ((a (b (c d))) (e f)) → Extraer c
```lisp
(car (car (cdr (car (cdr (car '((a (b (c d))) (e f))))))))
; o alternativamente:
(caar (cdr (cadr (car '((a (b (c d))) (e f))))))
```

### 13. Lista: ((1 (2 (3 (4 5)))) (6 7)) → Extraer 4
```lisp
(car (car (cdr (car (cdr (car (cdr (car '((1 (2 (3 (4 5)))) (6 7))))))))))
; o alternativamente:
(caar (cdr (car (cdr (cadr (car '((1 (2 (3 (4 5)))) (6 7))))))))
```

### 14. Lista: (((a b) c) ((d e) f) ((g h) i)) → Extraer g
```lisp
(car (car (car (cdr (cdr '(((a b) c) ((d e) f) ((g h) i)))))))
; o alternativamente:
(caar (caddr '(((a b) c) ((d e) f) ((g h) i))))
```

### 15. Lista: ((x y) (z w)) ((p q) (r s))) → Extraer r
```lisp
(car (car (cdr (car (cdr '(((x y) (z w)) ((p q) (r s))))))))
; o alternativamente:
(caar (cdr (cadr '(((x y) (z w)) ((p q) (r s))))))
```

### 16. Lista: (((1 (2 (3 (4 (5 6))))) (7 8)) → Extraer 5
```lisp
(car (car (cdr (car (cdr (car (cdr (car (cdr (car '((1 (2 (3 (4 (5 6))))) (7 8))))))))))))
; o alternativamente:
(caar (cdr (car (cdr (car (cdr (cadr (car '((1 (2 (3 (4 (5 6))))) (7 8)))))))))
```

### 17. Lista: (((a (b (c (d e)))) (f g)) → Extraer d
```lisp
(car (car (cdr (car (cdr (car (cdr (car '(((a (b (c (d e)))) (f g))))))))))
; o alternativamente:
(caar (cdr (car (cdr (cadr (car '(((a (b (c (d e)))) (f g))))))))
```

### 18. Lista: (((1 2) (3 4)) ((5 6) (7 8))) → Extraer 7
```lisp
(car (car (cdr (car (cdr '(((1 2) (3 4)) ((5 6) (7 8))))))))
; o alternativamente:
(caar (cdr (cadr '(((1 2) (3 4)) ((5 6) (7 8))))))
```

### 19. Lista: ((x (y (z (w v))))) → Extraer w
```lisp
(car (car (cdr (car (cdr (car (cdr (car '((x (y (z (w v))))))))))))
; o alternativamente:
(caar (cdr (car (cdr (cadr (car '((x (y (z (w v))))))))))
```

### 20. Lista: (((a b c) (d e f)) ((g h i) (j k l))) → Extraer j
```lisp
(car (car (cdr (car (cdr '(((a b c) (d e f)) ((g h i) (j k l))))))))
; o alternativamente:
(caar (cdr (cadr '(((a b c) (d e f)) ((g h i) (j k l))))))
```

## Notas importantes:

1. **car**: Extrae el primer elemento de una lista
2. **cdr**: Extrae todo excepto el primer elemento (la "cola" de la lista)
3. Las funciones compuestas como `caddr`, `cadr`, `caar`, etc. son abreviaciones:
   - `cadr` = `(car (cdr ...))`
   - `caddr` = `(car (cdr (cdr ...)))`
   - `caar` = `(car (car ...))`
   - `cadar` = `(car (cdr (car ...)))`

4. Para navegar estructuras anidadas complejas, es útil trabajar de afuera hacia adentro, identificando qué operaciones `car` y `cdr` necesitas aplicar en secuencia.

5. Siempre puedes usar las formas expandidas con `car` y `cdr` explícitos si las abreviaciones te resultan confusas.