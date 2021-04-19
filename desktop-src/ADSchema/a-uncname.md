---
title: UNC-Name 屬性
description: 共用磁片區和印表機的通用命名慣例名稱。
ms.assetid: 967fd0dc-10af-4482-bc2c-1d1dc13dee39
ms.tgt_platform: multiple
keywords:
- UNC-Name 屬性 AD 架構
- uNCName 屬性 AD 架構
topic_type:
- apiref
api_name:
- UNC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e06bc54ebb035a491e2d93a1c372e2d46fc43f76
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106976987"
---
# <a name="unc-name-attribute"></a>UNC-Name 屬性

共用磁片區和印表機的通用命名慣例名稱。



| 進入 | 值 |
|-------------------|-----------------------------------------------|
| CN                | UNC-Name                                      |
| Ldap-顯示名稱 | uNCName                                       |
| 大小              | \-                                            |
| 更新許可權  | 網域系統管理員                          |
| 更新頻率  | 當新的磁片區或列印佇列建立時。 |
| Attribute-Id      | 1.2.840.113556.1.4.137                        |
| 系統識別碼-Guid    | bf967a64-0de6-11d0-a285-00aa003049e2          |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)   |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                           |
| 中使用的類別        | [**索引-伺服器-目錄**](c-indexservercatalog.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**磁碟區**](c-volume.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                        |
| MAPI-Id                | \-                                                                                                                                                                                        |
| System-Only            | 否                                                                                                                                                                                     |
| 是-單一值       | 對                                                                                                                                                                                      |
| 已編制索引             | 對                                                                                                                                                                                      |
| 在通用類別目錄中      | 對                                                                                                                                                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                        |
| Search-Flags           | 0x00000001                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                |
| 中使用的類別        | [**FT-Dfs**](c-ftdfs.md)<br/> [**索引-伺服器-目錄**](c-indexservercatalog.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**磁碟區**](c-volume.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**FT-Dfs**](c-ftdfs.md)<br/> [**索引-伺服器-目錄**](c-indexservercatalog.md)<br/> [**毫秒-列印-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**磁碟區**](c-volume.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**FT-Dfs**](c-ftdfs.md)<br/> [**索引-伺服器-目錄**](c-indexservercatalog.md)<br/> [**毫秒-列印-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**磁碟區**](c-volume.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**FT-Dfs**](c-ftdfs.md)<br/> [**索引-伺服器-目錄**](c-indexservercatalog.md)<br/> [**毫秒-列印-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**磁碟區**](c-volume.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**FT-Dfs**](c-ftdfs.md)<br/> [**索引-伺服器-目錄**](c-indexservercatalog.md)<br/> [**毫秒-列印-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**磁碟區**](c-volume.md)<br/> |



 

 





