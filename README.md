# app-helm

## Estrutura e Arquivos
```
.
├── Chart.yaml <-- Arquivo onde se insere a versão do Chart e a Versão da aplicação
├── README.md
├── templates <-- Local onde ficam todos os arquivos de template dos manifestos
│   ├── _helpers.tpl
│   ├── configmap.yaml
│   ├── cronJob.yaml
│   ├── deployment.yaml
│   ├── hpa.yaml
│   ├── ingress.yaml
│   ├── namespace.yaml
│   ├── secret.yaml
│   ├── service.yaml
│   └── statefulset.yaml
└── values.yaml <-- Arquivo onde estão as configurações que serão passadas para os templates, nesse arquivo existem comentarios com as instruções de como ativar e desativar essas configurações, dentro dos cenarios de frontend, backend, Cronjobs e statefulSet
```

## Como Instalar

### Instalando com dry run, para testar para visualizar os manifestos que serão aplicados 

```
cd helm-sample
helm upgrade -i test --dry-run --namespace test --values values.yaml .
```

###  Instalando o helm, sem dry run
```
cd helm-sample
helm upgrade -i test  --namespace test --values values.yaml .

```
