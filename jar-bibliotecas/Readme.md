# Empacotamento em arquivos JAR e uso de bibliotecas

### Arquivo JAR

Java ARchive (JAR) é um arquivo compactado com um conjunto de classes e outros recursos (imagens,áudio, etc) e usado para distribuir aplicativos ou bibliotecas Java.

No arquivo build.gradle, de um projeto Java em Gradle, é necessário inserir o seguinte bloco:

```java
 jar { 
     manifest {
        // Classe principal da aplicação 
        attributes "Main-Class": "poo.Principal"
    } 
}
```

### Dependência de bibliotecas com o Gradle

```java
dependencies {
 testImplementation 'junit:junit:4.12'

 // https://bintray.com/bintray/jcenter/com.google.zxing%3Acore
 implementation 'com.google.zxing:core:3.4.0'

 // https://bintray.com/bintray/jcenter/com.google.zxing%3Ajavase
 implementation 'com.google.zxing:javase:3.4.0'

 // importando arquivo JAR que est´a dentro do diret´orio libs
 implementation files('libs/biblioteca.jar')
}
```

