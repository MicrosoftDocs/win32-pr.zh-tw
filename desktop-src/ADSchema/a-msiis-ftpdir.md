---
title: ms-IIS-FTP-Dir 屬性
description: 這個屬性會決定相對於檔案伺服器共用的使用者主目錄。 它會與 ms-IIS-FTP 根目錄搭配使用，以判斷 FTP 使用者主目錄。
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- ms-IIS-FTP-Dir 屬性 AD 架構
- msIIS-FTPDir 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509608"
---
# <a name="ms-iis-ftp-dir-attribute"></a>ms-IIS-FTP-Dir 屬性

這個屬性會決定相對於檔案伺服器共用的使用者主目錄。 它會與 ms-IIS-FTP 根目錄搭配使用，以判斷 FTP 使用者主目錄。



| 進入 | 值 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-IIS-FTP-Dir                                                                                                                  |
| Ldap-顯示名稱 | msIIS-FTPDir                                                                                                                    |
| 大小              | 30-50 個字元針對每個屬性 (15-25 Unicode 字元)                                                                    |
| 更新許可權  | 網域系統管理員 & 本機系統                                                                                             |
| 更新頻率  | 當系統管理員建立網站並設定 FTP 隔離時，會設定此屬性。 這麼做之後很少會變更。 |
| Attribute-Id      | 1.2.840.113556.1.4.1786                                                                                                         |
| 系統識別碼-Guid    | 8a5c99e9-2230-46eb-b8e8-e59d712eb9ee                                                                                            |
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
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



 

 





