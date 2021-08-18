---
title: ms-IIS-FTP-根屬性
description: 這個屬性會決定檔案伺服器共用。 它會與 ms-IIS-FTP-Dir 搭配使用，以判斷 FTP 使用者主目錄。
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- ms-IIS-FTP-根屬性 AD 架構
- msIIS-FTPRoot 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4def81aa39c9df5aaa336a05514ab4581aa14533917fad008fc9c49d32d13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118682522"
---
# <a name="ms-iis-ftp-root-attribute"></a>ms-IIS-FTP-根屬性

這個屬性會決定檔案伺服器共用。 它會與 ms-IIS-FTP-Dir 搭配使用，以判斷 FTP 使用者主目錄。



| 進入 | 值 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-IIS-FTP-根目錄                                                                                                                 |
| Ldap-顯示名稱 | msIIS-FTPRoot                                                                                                                   |
| 大小              | 30-50 個字元針對每個屬性 (15-25 Unicode 字元)                                                                    |
| 更新許可權  | 網域系統管理員 & 本機系統                                                                                             |
| 更新頻率  | 當系統管理員建立網站並設定 FTP 隔離時，會設定此屬性。 這麼做之後很少會變更。 |
| Attribute-Id      | 1.2.840.113556.1.4.1785                                                                                                         |
| 系統識別碼-Guid    | 2a7827a4-1483-49a5-9d84-52e3812156b4                                                                                            |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



 

 





