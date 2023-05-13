# Freelancer-Proyecto
Creando una pagina freelancer con HTML y CSS

Para estructurar el texto de HTML son necesarias las siguientes tags:
    nav: 
        representa una sección de una página cuyo propósito es proporcionar enlaces de navegación, ya sea dentro del documento actual o a otros documentos. Ejemplos comunes de secciones de navegación son menús, tablas de contenido e índices.
    section:
        representa una sección genérica de un documento. Sirve para determinar qué contenido corresponde a qué parte de un esquema. Piensa en el esquema como en el índice de contenido de un libro; un tema común y subsecciones relacionadas. Es, por lo tanto, una etiqueta semántica. Su funcionalidad principal es estructurar semánticamente un documento a la hora de ser representado por parte de un agente usuario. Por ejemplo, un agente de usuario que represente el documento en voz, podría exponer al usuario el índice de contenido por niveles para navegar rápidamente por las distintas partes.
    article: 
        representa una composición auto-contenida en un documento, una página, una aplicación o en un sitio, que se quiere que sea distribuíble y/o reutilizable de manera independiente, por ejemplo, en la redifusión. Algunos ejemplos podrían ser un mensaje en un foro, un artículo de una revista o un periódico, una entrada de blog, el comentario de un usuario, un widget o gadget interactivo, o cualquier otro elemento de contenido independiente.
    aside:  
        representa una sección de una página que consiste en contenido que está indirectamente relacionado con el contenido principal del documento. Estas secciones son a menudo representadas como barras laterales o como inserciones y contienen una explicación al margen como una definición de glosario, elementos relacionados indirectamente, como publicidad, la biografía del autor, o en aplicaciones web, la información de perfil o enlaces a blogs relacionados.

    div:
        div Sirve para crear secciones o agrupar contenidos.
        Sus etiquetas son: <div> y </div> (ambas obligatorias).

        Está definido como: Elemento en bloque.

        Crea una caja: En bloque.

        Puede contener: Texto, y/o cero o más elementos en bloque o en linea.




propiedades para agregar en todos los proyectos:

PRecarga el CSS
    Para que nuestro css sea mas rapido en cargar, podemos PRECARGAR el archivo, para disminuir los tiempos, es necesario la siguiente tag en html:

    <link rel="preload" href="css/style.css" as="style">

    esto antes de linkear nuestro documento css



hack para REINICIAR el tamaño del documento y mejorar REM

    se creo un hack en el cual se selecciona les tags en CSS:

    -html, se renicia el tamaño a 62.5% (font-size)

    body se reinicia a 16px. (font-size)

    esas dos lineas permiten que los rems sean muy sencillos de utilizar y tengamos todo el potencial del rem, es mejor usar rem por que se adaptan mas a una gran cantidad de navegadores y nuevos dispositivos (tablets, relojes smathphones, tv etc)

    1rem = 10px


Pseudo-selectores (custom properties):

    inician con ':', son elementos que no existen como tal en html.

    :root -> Nos permite almacenar variables de css, que son conocidas como Custom properties (Propiedades personalizadas). Son entidades definidas por autores de CSS que contienen valores específicos para reutilizarlos en un documento. Se establecen utilizando la notación de propiedades personalizadas 
            (por ejemplo, --main-color: black;) 
    y se accede a ellos mediante la función var() 
            (por ejemplo, color: var(--main-color);

    Es recomendable agregarlo a nuestros documentos ya que facilitan los cambios que se puedan generar, algunos ejemplos serian: paleta de colores, fuentes, estilos, etc.


NORMALIZE
    Casi todos los navegadores mantienen ciertos estandares en los estilos por defecto, sin embargo hay algunos navegadores que no se riguen bajo esos estandares, en el mundo no solo hay navegadores actualizados, y cientos de personas entran a la web por medio de dispositivos antiguos y desactualizados. Estos factores hacen que los estilos por defecto cambien entre un navegador y otro, por eso es importante que en nuestro codigo sea normalizado, y que aunque nuestra pagina sea abierta en un navegador antiguo, el estilo no cambie. existen diferentes metodos para normalizar nuestra web, aunque el recomendable es descargar un archivo .css que contenga esos estandares (pag. para eso, buscar 'normalize.css'). es importante meter ese documento css en nuestro html (por medio del tag 'link' en la cabecera) ANTES de nuestro documento principal de CSS, que este sea el primer link incrustado en nuestro html.

buenas practicas:
    *Es una buena practica que en todos nuestros documentos CSS pongamos de inicio esta propiedad a todo el documento, garantizando asi que nuestras medidas de cajas se mantengan como nosotros las hemos declarado.

            *{
                box-sizing: border-box;
            }

    *Poner un margin 0; para restablecer los margenes por defecto del navegador, si asi se requiere en el body

            body{
                margin: 0;
            }



Sobre css
    -flex box: 
    
        fue diseñado como un modelo unidimensional (en una sola direccion) para crar layouts (diseños).

        tiene 2 ejes, solo puedes colocar y distribuir tus elementos en una direccion fila(rows) o columna (column)
        
        row es aplicado por default al definir un display: flex;

        este esta diseñado para alinear elementos en tus diseños

        En el diseño flex, los nodos hijo se pueden distribuir en dirección vertical u horizontal y se pueden "flexibilizar" sus tamaños, bien sea rellenando el espacio disponible o encogiéndose para evitar salirse del contorno del nodo padre. Se puede manipular fácilmente tanto la alineación horizontal como la vertical, de los nodos hijo. La anidación de estas cajas (horizontal dentro de vertical o vertical dentro de horizontal) se puede usar para construir diseños en dos dimensiones.

        propiedades dentro de flex:
            justify-content
            align-items
            gap
            flex-grow
            flex-basis
            flex-direction


    -Metodologias o formas de escribir CSS
        
        BEM
        Utility First
        Modulos


    -Responsive Web Design y Media Queries

        -Hacer tu sitio web adaptable a diferentes Dispositivos.

        -Algunos enfoques anteriores, era crear un 
        
            
        sitio web principal (para laptops, compus), 
            sitioweb.com
        otro para sitio para celulares, 
            mobile.sitioweb.com
        otro para tablets. 
            tablet.sitioweb.com

        Este enfoque fue popular hace unos años, pero termino siendo dificil, ya que en lugar de mantener un solo sitio web, mantenias 3 o 4.

        Es importante hacer 'responsive' (adaptable) nuestros sitios web ya que google penaliza que no sean responsive.

        La solucion para evitar crear multiples sitios web y que sean adaptables a una gran cantidad de dispositivos es: 'Responsive Web Design con Media Queries'

        Responsive Web Desig:
        Es un enfoque que nos dice que nuestros diseños deberan adaptarse a las interacciones del usuario y la resolucion que utilizan.

        Como se logra esto?
        Con Media Queries, estos tienen una sintaxis de la siguiente forma:
            @media (mid-width: 768px){

            }
            @media (mid-width: 992px){

            }    
            
        los 'min-width' determina el tamaño de pantalla en el que se va aplicar el codigo que pongamos dentro de las llaves, por ejemplo:

        tenemos nuestra pagina web, y queremos que de 480px para arriba (500px, 600px,etc) nuestra pagina web sea color azul, para eso tenemos que escribir el siguiente codigo:

            @media (mid-width: 480px) {
                background-color: blue;
            }

        Existen algunos estandares de tamaños en los media queries, como lo son:

        mid-width: 
        768px: para tablets
        480px: movil
        1140px: laptop
        1400px: 


    -position
    -linear gradient
