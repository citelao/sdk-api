---
UID: TP:cimfs
ms.author: windowssdkdev
ms.date: 09/09/2019
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# CimFS

## -description

A CIM is a file-backed image format similar in concept to a WIM or a read-only VHD.

A CIM image consists of a small collection of flat files that include one or more data and metadata region files, one or more object ID files and one or more filesystem description files. As a result of their “flatness” CIMs are faster to construct, extract and delete than the equivalent raw directories they contain.

CIMs are composite in that a given image can contain multiple file system volumes which can be mounted individually while sharing the same data region backing files.

CIMs support deduplication at the file level. The CIMFS file system supports many of the constructs of NTFS such as security descriptors, alternate data streams, hard links and reparse points.

Once constructed, a CIM can be mounted with the support of the CIMFS driver. The mount constructs a read-only disk and file system volume device for the image. The contents of a mounted CIM can be accessed read-only using the standard Win32 or NT API file system interface.

CIMs were designed and optimized to be used as a Windows Container image layout.

To develop with CimFS, you need this header:

 * [cimfs.h](../cimfs/index.md)

