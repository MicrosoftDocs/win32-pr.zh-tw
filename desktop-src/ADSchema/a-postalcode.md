---
title: Postal-Code 屬性
description: 郵件傳遞的郵遞區號或郵遞區號。
ms.assetid: bc8c4f52-df95-4676-beee-e6b86ba668a9
ms.tgt_platform: multiple
keywords:
- Postal-Code 屬性 AD 架構
- 郵遞區號屬性 AD 架構
topic_type:
- apiref
api_name:
- Postal-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284295797c3ca5449fad72a834bd46c460b51cb7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991316"
---
# <a name="postal-code-attribute"></a>Postal-Code 屬性

郵件傳遞的郵遞區號或郵遞區號。



| 進入 | 值 |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Postal-Code                                                                 |
| Ldap-顯示名稱 | postalCode                                                                  |
| 大小              | \-                                                                          |
| 更新許可權  | 網域系統管理員或帳戶擁有者。                                      |
| 更新頻率  | 當使用者的記錄建立時，以及每次需要變更的位址時。 |
| Attribute-Id      | 2.5.4.17                                                                    |
| 系統識別碼-Guid    | bf9679fd-0de6-11d0-a285-00aa003049e2                                        |
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
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                          |
| System-Only            | 否                                                                                                                                                                                                                                                                                                           |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                            |
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
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                    |
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
| MAPI-Id                | 0x3A2A                                                                                                           |
| System-Only            | 否                                                                                                            |
| 是-單一值       | 對                                                                                                             |
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
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                    |
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
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                    |
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
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                    |
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
| MAPI-Id                | 0x3A2A                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 對                                                                                                                                                                                                                                                                                                                                                                    |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





