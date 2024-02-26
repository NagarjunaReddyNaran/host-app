ng new mono-workspace --create-application="false"
cd mono-workspace
ng g application host-app --routing --style=scss
ng g application mfe-app --routing --style=scss

ng s host-app -o
ng s mfe-app -o

npm i webpack webpack-cli --save-dev

ng add @angular-architects/module-federation@15 --project host-app --port 4200
ng add @angular-architects/module-federation@15 --project remote-app --port 4300