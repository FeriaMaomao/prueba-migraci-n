1. Escribe un comando para ver las últimas dos líneas del archivo `lorem-ipsum.txt`, ubicado en el directorio `bash/`:
```respuesta 
tail -2 bash/lorem-ipsum.txt
```

2. Escribe un comando para mostrar la cantidad de palabras que contiene cada línea del archivo `lorem-ipsum.txt`, ubicado en el directorio `bash/`:
```respuesta
linea=$(wc -l bash/lorem-ipsum.txt | awk '{print $1}') \ 
i=1
while [ $i -le $linea ]
do
    echo "La linea $i contiene" $(sed -n "$i"p ./bash/lorem-ipsum.txt | wc -m) "caracteres"
    ((i++))
done
```

1. Escribe un comando para ver el contenido del archivo `lorem-ipsum.txt`, ubicado en el directorio `bash`, sin los caracteres ***punto*** `.` y ***coma*** `,`:
```respuesta
sed 's/[.,]//g' bash/lorem-ipsum.txt
```

4. Escribe un comando para listar todos los directorios dentro de este repositorio (no recursivo):
```respuesta
ll * ../prueba-tecnica-main

tree ../prueba-tecnica-main
```

5. Esribe un comando para ordenar los directorios listados, por tamaño:
```respuesta
ll * -Sr ../prueba-tecnica-main

ll -RSr ../prueba-tecnica-main
```
