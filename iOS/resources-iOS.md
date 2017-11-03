## iOS

### Sommaire

1. [Liens utiles](#liens_utiles)
2. [Outil](#outil)
3. [Script](#script)

### Liens utiles

- [NSHispter](http://nshipster.com/)

    Blog généraliste qui traite de nombreux sujets liés à iOS (Swift, Cocoa, ...).
    Même si le blog n'est plus régulièrement tenu à jour de nombreux articles valent le coup d'oeil.
    
- [RayWenderlich](https://www.raywenderlich.com/)

    Site qui contient de nombreux tutorials, les tutorial sont régulièrement mis à jour pour être en accords avec
    les versions d'iOS et de Swift.
    Les tutorials sont aux format article/vidéo, une partie du contenu vidéo est payant.

- [objc.io](https://www.objc.io/)
    
    Site qui contient de nombreux articles qui expliquent en détails le fonctionnement/fonctionnement de certains 
    framework du SDK iOS. Depuis 2016 le format à changer pour passer sur des vidéos qui abordent divers sujet liés au
    développement Swift. Une partie du contenu vidéo est payant.

- [LittleBitesOfCocoa](https://littlebitesofcocoa.com/)

    Blog généraliste qui poste regulièrement de petits articles liés à iOS (Swift, CocoaTouch, ...).
  
- [F*ckingBlockSyntax](http://fuckingblocksyntax.com/)

    Pense bête pour la syntaxe un peu compliqué des block Objective-C
    
- [F*ckingClangWarnign](http://fuckingclangwarnings.com/)

    Site qui recense l'ensemble des warning clang avec leur message associée.
    
- [OSSatus](https://www.osstatus.com/)
    
    Site qui recense les codes d'erreur Apple.

- [Liste des tailles d'iPhone](http://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions)


### Outil

- [Injection](http://johnholdsworth.com/injection.html)

    Outil qui permet de recompiler des projets iOS à la volé.

### Script

#### 1. Transformer les TODOS en warning

```shell
TAGS="TODO|FIXME|HACK"
echo "searching ${SRCROOT} for ${TAGS}"
find "${SRCROOT}" \( -name "*.h" -or -name "*.m" -or -name "*.swift" \) -not -path "${SRCROOT}/Pods/*" -print0 | xargs -0 egrep --with-filename --line-number --only-matching "($TAGS).*\$" | perl -p -e "s/($TAGS)/ warning: \$1/"
```

Permet de générer des warnings si un fichier contient un TODO, FIXME ou HACK. Le script ignore le repertoire des Pods pour ne pas générer de warning inutiles.


