# Azure

## Azure CLI

### Initial steps

#### Check version

```az version```

#### Login

```az login```

#### Find commands

```az find```

#### Resource group

```az group create –location x –name y```
```az group list```
```az group delete –name y```

#### Service plan

```az appservice plan create –name z –resource-group y –sku a [--is-linux|?]```

#### Runtimes

```az webapp list-runtimes```

#### Web app

```az webapp create –name b –plan z –resource-group y –runtime c```
```az webapp browse -n b –resource-group y```


