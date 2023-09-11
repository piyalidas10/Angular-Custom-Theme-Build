# Angular Theme Build

## ngx-build-plus package
Extend the Angular CLI's default build behavior without ejecting: 📄 Extend the default behavior by providing a partial config that just contains your additional settings.
Reference URL : https://github.com/manfredsteyer/ngx-build-plus


## Error scenarios
### peer dependency error

When getting peer dependency error run below command
npm install --legacy-peer-deps
It will override all the dependencies in package.lock.json & package.json file of your project.


### share module error

Error "shared module is not available for eager consumption"

Bootstrapping is required.
just moved the original main.ts content to the new file bootstrap.ts and update main.ts to:
import('./bootstrap').catch((error) => console.error(error));

### Angular upgrade from 12 to 14
First upgrade the @angular-eslint/schematics package
```
ng update @angular-eslint/schematics@14
```

Upgrade Angular
```
ng update @angular/core@14 @angular/cli@14
```

@angular-eslint/schematics - Schematics which are used to add and update configuration files which are relevant for running ESLint on an Angular workspace.

