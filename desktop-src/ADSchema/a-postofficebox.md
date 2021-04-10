---
title: 郵局-Box 屬性
description: 此物件的郵局箱號碼。
ms.assetid: e782271a-2f79-42af-9c62-5723917a6f47
ms.tgt_platform: multiple
keywords:
- 郵局-Box 屬性 AD 架構
- postOfficeBox 屬性 AD 架構
topic_type:
- apiref
api_name:
- Post-Office-Box
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc8edd327a8b7577e7a8256a8e2f082aad13c8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935504"
---
# <a name="post-office-box-attribute"></a>郵局-Box 屬性

此物件的郵局箱號碼。



| 進入 | 值 |
|-------------------|-----------------------------------------------------------------------------|
| CN                | 郵局-Box                                                             |
| Ldap-顯示名稱 | postOfficeBox                                                               |
| 大小              | \-                                                                          |
| 更新許可權  | 網域系統管理員或帳戶擁有者。                                      |
| 更新頻率  | 當使用者的記錄建立時，以及每次需要變更的位址時。 |
| Attribute-Id      | 2.5.4.18                                                                    |
| 系統識別碼-Guid    | bf9679fb-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                          |
| System-Only            | 否                                                                                                                                                                                                                                                                                                           |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                           |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                               |
| MAPI-Id                | 0x3A2B                                                                                                           |
| System-Only            | 否                                                                                                            |
| 是-單一值       | 否                                                                                                            |
| 已編制索引             | 否                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 40                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





