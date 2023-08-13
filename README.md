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

