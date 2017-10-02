# Checklist d'init de projet JS / TS

- Utiliser la CLI (Angular / Vue / React)
- Faire un eject selon les besoins du projet
- Mettre un .npmrc avec `save-prefix='~'` à minima.
- Mettre un [.nvmrc](https://github.com/creationix/nvm#nvmrc) avec la version de Node
- Mettre [ESLint](https://eslint.org/) (ou [TSLint](https://palantir.github.io/tslint/))
- Mettre [Prettier](https://github.com/prettier/prettier)
- Dans le package.json, se faire un script de test, un de build, et des scripts de pre/post tag
```
"preversion": "npm run test",
"postversion": "git push && git push --tags"
```