LRU
Una memoria caché de uso menos reciente (LRU) organiza los elementos en orden de uso, lo que le permite identificar rápidamente qué elemento no se ha utilizado durante más tiempo.
int main()
{

    my_buffer.request_page(pointer_a);
    my_buffer.request_page(pointer_b);
    my_buffer.request_page(pointer_a);
    my_buffer.request_page(pointer_c);
    my_buffer.request_page(pointer_d);
    my_buffer.request_page(pointer_e);
    my_buffer.request_page(pointer_a);
    my_buffer.request_page(pointer_b);
    my_buffer.request_page(pointer_c);
    my_buffer.request_page(pointer_a);
    /*
    a a a a a e e e c
      b b b d d d b b
          c c c a a a
    */
    my_buffer.print_buf_pages();
 
    return 0;
}




FUNCIONAMIENTO DEL CÓDIGO
Para la ejecución del código del LRU caché,según nuestra interfaz principal:
Primero crearemos una instancia del LRU, con el nombre de my_buffer(), éste recibirá un parámetro de entrada que será el número de frame que mi LRU cache tendrá..
Luego ingresamos las páginas o registros que se almacenarán en disco, pero para esto, les asignamos un puntero, para que ocupe menos espacio de memoria al momento de almacenarlo en disco..
Por último ingresamos según la secuencia que tengamos al usar las páginas o al ser llamadas en memoria, por ende ingresamos cada una de ellas, para que en este paso según nuestro function request_page(), cambie o reemplace la página usada con más tiempo en nuestro disco.
Al final, se imprimirán en la consola, los elementos o páginas que quedaron en el buffer pool..
