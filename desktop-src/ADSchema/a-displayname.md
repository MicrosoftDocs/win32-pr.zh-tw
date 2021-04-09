---
title: Display-Name 屬性
description: 物件的顯示名稱。
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Display-Name 屬性 AD 架構
- displayName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4fe662ccbdf2157c7ed51a311739cf7d16273b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686807"
---
# <a name="display-name-attribute"></a>Display-Name 屬性

物件的顯示名稱。 這通常是使用者名字、中間名和姓氏的組合。



| 進入 | 值 |
|-------------------|------------------------------------------------------------------------------|
| CN                | 顯示名稱                                                                 |
| Ldap-顯示名稱 | displayName                                                                  |
| 大小              | \-                                                                           |
| 更新許可權  | 網域系統管理員或帳戶擁有者。                                       |
| 更新頻率  | 當使用者的記錄建立時，以及顯示名稱需要變更時。 |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| 系統識別碼-Guid    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                  |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                            |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                             |
| 已編制索引             | 對                                                                                                                                                                                                                                                                                                                                             |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| 中使用的類別        | [**通訊錄-容器**](c-addressbookcontainer.md)<br/> [**位址範本**](c-addresstemplate.md)<br/> [**PKI-憑證-範本**](c-pkicertificatetemplate.md)<br/> [**服務類別**](c-serviceclass.md)<br/> [**服務實例**](c-serviceinstance.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**通訊錄-容器**](c-addressbookcontainer.md)<br/> [**位址範本**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-憑證-範本**](c-pkicertificatetemplate.md)<br/> [**服務類別**](c-serviceclass.md)<br/> [**服務實例**](c-serviceinstance.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 對                            |
| 已編制索引             | 對                            |
| 在通用類別目錄中      | 對                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 0                               |
| Range-Upper            | 256                             |
| Search-Flags           | 0x00000005                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**通訊錄-容器**](c-addressbookcontainer.md)<br/> [**位址範本**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-憑證-範本**](c-pkicertificatetemplate.md)<br/> [**服務類別**](c-serviceclass.md)<br/> [**服務實例**](c-serviceinstance.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**通訊錄-容器**](c-addressbookcontainer.md)<br/> [**位址範本**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-憑證-範本**](c-pkicertificatetemplate.md)<br/> [**服務類別**](c-serviceclass.md)<br/> [**服務實例**](c-serviceinstance.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**通訊錄-容器**](c-addressbookcontainer.md)<br/> [**位址範本**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-憑證-範本**](c-pkicertificatetemplate.md)<br/> [**服務類別**](c-serviceclass.md)<br/> [**服務實例**](c-serviceinstance.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 已編制索引             | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| 中使用的類別        | [**通訊錄-容器**](c-addressbookcontainer.md)<br/> [**位址範本**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-憑證-範本**](c-pkicertificatetemplate.md)<br/> [**服務類別**](c-serviceclass.md)<br/> [**服務實例**](c-serviceinstance.md)<br/> [**返回頁首**](c-top.md)<br/> |



 

 





