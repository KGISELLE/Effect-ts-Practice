## Paso a paso practica Effect-ts
Para realizar esta primera parte se toma como base la guia de inicio rapido encontrada en la
[documentacion de effect-ts](https://effect.website/docs/quickstart).
1. Crear el repositorio.
2. Ya dentro del repositorio abrir la terminal. 
3. Por medio de la terminar comenzar la configuracion inicial del proyecto.
4. Crear el archivo package.json con el siguiente comando, digitandolo en la terminal:
    ```
    npm init -y
    ```
5. Instalar Typescript
    ```
    npx install typescript
    //or
    npm install --save-dev typescript
    ```
6. Inicializar TypeScript en el proyecto
    ```
    npx tsc --init
    ```
    Esto crea un archivo `tsconfig.json`, el cual contiene la configuracion de TS. Al entrar a este archivo hay que acegurarse que "strict:" sea true,
7. Instalar el paquete Effect como dependencia
    ```
    npm install effect
    ```
8. Crear la estructura inicial del proyecto (arquitectura: carpetas y archivos del proyecto).
    * Crear la carpeta `src`
    * Crear el archivo `index.ts` dentro de la carpeta `src`
9. Probar si funcion Effect-ts en nuestro proyecto, es decir si la instalación quedo correcta. 
    * Agregar el siguiente codigo en `src/index.ts`
        ```ts
        import { Effect, Console } from "effect"
 
        const program = Console.log("Hello, World!")
 
        Effect.runSync(program)
        ```

10. Ejecutar el archivo `index.ts`.
    * Para esto si se tiene instalado ts-node ejecutar el siguiente comando en la terminal:
        ```
        ts-node src/index.ts
        ```
    Deberías ver el mensaje "Hello, World!" impreso en la terminal. Esto confirma que el programa está funcionando correctamente.
    * De lo contrario instalar ts-node con el siguiente comando:
        ```
        npx ts-node
        ```
        No me funciono con el anterior comando porque me generaba un error, asi que proble instalandolo como dependencia de desarrollo
        ```
        npm install -D ts-node
        ```

11. Para poder hacer mi primer commit, hay que inicializar git para comenzar un control de versiones, con el siguiente comando:
    ```
    git init
    ```
12. Pero antes de inicializar git coloque la carpeta de node_modulos como oculta para que no se suba al control de versiones., para esto hay que cregar un archivo `.gitignore` en la root del proyecto y dentro de este archivo colocar la carpeta que queremos ocultar, asi:
    ```
    node_modules/
    ```
13. Agregar al control de versiones los paquetes y los archivos creados hasta el momento:
    ```
    git add .
    ```