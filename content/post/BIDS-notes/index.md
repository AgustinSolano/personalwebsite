---
authors:
- admin
categories:
- Demo
date: "2021-02-15T00:00:00Z"
draft: false
featured: false
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ""
  placement: 2
  preview_only: false
date: "2021-02-15T00:00:00Z"
projects: []
summary: "La estructura para datos de neuroimagenes es un estándar para organizar, anotar, y describir los datos recogidos en experimentos de neurociencias."
tags:
- Academic
- Tutorial
title: Comenzar a usar la Brain Imaging Data Structure (BIDS)
---

## Que es BIDS?
BIDS: Brain Imaging Data Structure es una forma de estructurar todos los datos obtenidos en experimentos de Neuroimágenes (MRI, fMRI, EEG, iEEG, conducta, etc)

Un ejemplo de como quedaría organizado el arbol de directorios se puede ver en esta imagen:

{{< figure src="bids_dir_tree_2.jpg" title="Estructura de directorios acorde a BIDS" >}}

La recomendación es ingresar primero al [sitio principal del estándar ](https://bids.neuroimaging.io/ "BIDS") y mirar también los [detalles del estándar (v1.4.0)](https://bids-specification.readthedocs.io/en/stable/ "v1.4.0") para entender el árbol de directorios y archivos requeridos.

**Video-tutoriales** como para arrancar:

* [The benefits of BIDS](https://youtu.be/K9hVAr5fvJg) - BrainHack 2020 de OHBM
* [Brain Imaging Data Standards BIDS for EEG](https://youtu.be/DUufZLhl7jM) - Dr. Cyril Pernet, Sapiens Lab

A continuación voy a listar algunos de los recursos mas útiles que vaya encontrando y una breve descripción:

* [**BIDS Starter Kit**](https://github.com/bids-standard/bids-starter-kit): Como primer paso recomiendo ingresar al [BIDS Starter Kit](https://github.com/bids-standard/bids-starter-kit). Es un repositorio alojado en github con lo necesario para arrancar.
  + [**BIDS wiki**](https://github.com/bids-standard/bids-starter-kit/wiki): La [wiki](https://github.com/bids-standard/bids-starter-kit/wiki) tiene varios recursos básicos para introducirse a la filosofía en la que se basa el estándar, los tipos de archivos principales que se usan para enriquecer la info que se registra de nuestros datos. También hay tutoriales, datasets de ejemplo, presentaciones/recursos/links para profundizar.
  + [**Validador del formato**](https://bids-standard.github.io/bids-validator/): Una herramienta muy importante es el [validador](https://bids-standard.github.io/bids-validator/) que nos permite verificar si un dataset cumple con los requerimientos de BIDS. 
  + [**Comunidad Neurostars**](https://neurostars.org/tags/bids): Para tener la posibilidad de hacer preguntas y contactar a la comunidad recomiendan el uso de la plataforma [Neurostars](https://neurostars.org/tags/bids). Alli también se pueden hacer consultas sobre otras ramas de neuroimágenes.
  + [**BIDS Apps**](http://bids-apps.neuroimaging.io/apps/): Otra cosa muy útil son una serie de apps ([BIDS Apps](http://bids-apps.neuroimaging.io/apps/)), que reciben como entrada un dataset organizado siguiendo BIDS y permiten aplicar un pipeline de procesamiento determinado. Las apps viene enpaquetadas en imágenes de Docker/Singularity. Hay varios desarrollos ya disponibles para usar, aunque la mayoría son para MRI/fMRI.

* [**PyBIDS**](https://github.com/bids-standard/pybids) es una librería con funciones para interactuar con BIDS, usando python. Permite crear un layout del dataset para poder recorrerlo y acceder a los archivos. Tiene funcionalidades para crear un reporte y finalmente herramientas para crear modelos lineales (GLMs) a partir del dataset.

* [**Repositorio de Robert Oostenveld**](https://github.com/robertoostenveld/bids-tools): Un repositorio que me ayudó mucho a organizar mis datos es el de [Robert Oostenveld](https://github.com/robertoostenveld/bids-tools). Tiene una serie de scripts para organizar/reorganizar archivos. Me resultó muy útil uno que permite crear todos los archivos accesorios del dataset (create sidecar files), en caso de que haya faltantes (incorpora los obligatorios y algunos opcionales). También permite chequear si está todo bien de acuerdo al estándar.
