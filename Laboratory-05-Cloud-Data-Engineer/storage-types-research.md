# Storage Types Research

Cloud storage can be divided into three primary types: Block Storage, File Storage, and Object Storage. Each type stores and provides access to data differently.

| Storage Type       | Description                                                                                                                                         | Primary Use Case                                                                           | Cloud Provider Example |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | ---------------------- |
| **Block Storage**  | Stores data as fixed-size blocks that can be independently managed. It behaves like a disk or hard drive attached to a computer or virtual machine. | Operating-system disks, databases, and applications that require low-level disk access.    | AWS EBS                |
| **File Storage**   | Stores data in a hierarchical file and folder structure that can be accessed and shared through a network.                                          | Shared files, directories, and applications that need a traditional file-system interface. | AWS EFS                |
| **Object Storage** | Stores data as objects together with metadata and a unique identifier. It is designed for large amounts of unstructured data.                       | Images, videos, backups, documents, and other large collections of unstructured data.      | AWS S3                 |

## Why Object Storage Is the Best Choice for the Client

Object Storage is a good choice for the client's photo-sharing application because user-uploaded images are unstructured data and the application may need to store millions of files. It provides a storage model designed for large collections of objects and keeps the images separate from the web-server container.
