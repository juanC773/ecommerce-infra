# E-commerce Infrastructure - Kubernetes

Este repositorio contiene los manifiestos de Kubernetes para desplegar los microservicios en diferentes ambientes.

## Estructura

```
ecommerce-infra/
├── k8s/                    # Manifests Kubernetes
│   ├── namespace.yaml
│   ├── service-discovery/
│   ├── cloud-config/
│   ├── product-service/
│   │   ├── deployment.yaml
│   │   └── configmap.yaml
│   └── README.md
└── README.md
```

## Separación de Responsabilidades

- **Este repositorio (`ecommerce-kubernetes`)**: Contiene los manifests de Kubernetes
- **`infra-torres`**: Contiene la infraestructura como código con Terraform (AKS, VNets, etc.)

## Uso

Ver `k8s/README.md` para instrucciones de despliegue.

## Orden de Despliegue

1. **Terraform** (desde `infra-torres`): Crear la infraestructura de Azure (AKS, VNets)
2. **Kubernetes Manifests** (este repo): Desplegar los microservicios en el cluster
