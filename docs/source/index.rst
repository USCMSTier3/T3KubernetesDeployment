.. USCMST3 Kubernetes Deployment documentation master file, created by
   sphinx-quickstart on Tue May 12 07:22:54 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to USCMST3 Kubernetes Deployment's documentation!
=========================================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:



#Indices and tables
#==================
#
#* :ref:`genindex`
#* :ref:`modindex`
#* :ref:`search`

Introduction
============
The following documentation describes the steps followed in order to deploy a USCMS Tier-3 on top of Kubernetes, via SLATE.

`Kubernetes <https://kubernetes.io/>`_ is an industrial open-source container-orchestration system for automating application deployment, scaling, and management. It was originally designed by Google, and is now maintained by the Cloud Native Computing Foundation.

The `SLATE project <https://slateci.io/>`_ enables a federated "NoOPs" operations model that gives cyberinfrastructure developers the flexibility to innovate at scale, expanding the reach of domain specific science gateways and multi-site research platforms. It supports several T3-related components in its `app list <https://portal.slateci.io/applications>`_, like Hosted CEs, HTCondor, OSG Frontier SQUID, etc.


Requirements
============
The following sets of requirements are necessary in order to use SLATE:

- Docker: Needed to start the SLATE container images for the services
- Kubernetes: To orchestrate the containers.
- At least 1 machine: To deploy the kubernetes (k8s) master, which will be in contact with the SLATE server, this machine (or others) can serve as the workers too to deploy your T3 components too.
- 2 Public Ips: The first for the k8s master, so the SLATE server can contact it. The second, for the ingress controller of the k8s load balancer (more on this, later).

Docker and Kubernetes Installation
==================================
