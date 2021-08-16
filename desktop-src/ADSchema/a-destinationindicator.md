---
title: Destination-Indicator 屬性
description: 這是 X. 500 規格的一部分，而且不是由 NTDS 使用。
ms.assetid: 3c8c8df1-25d7-4ef6-bec4-66b12318b3f0
ms.tgt_platform: multiple
keywords:
- Destination-Indicator 屬性 AD 架構
- destinationIndicator 屬性 AD 架構
topic_type:
- apiref
api_name:
- Destination-Indicator
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e9869296d9d1d09400d2ff0ba68953acb107e62ed6d58a716f3d8d6afc504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508998"
---
# <a name="destination-indicator-attribute"></a>Destination-Indicator 屬性

這是 X. 500 規格的一部分，而且不是由 NTDS 使用。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | Destination-Indicator                |
| Ldap-顯示名稱 | destinationIndicator                 |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 2.5.4.27                             |
| 系統識別碼-Guid    | bf967951-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**String(IA5)**](s-string-ia5.md)  |



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
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                          |
| System-Only            | 否                                                                                                                                                                                                                                                                                                           |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                           |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                               |
| MAPI-Id                | 0x8070                                                                                                           |
| System-Only            | 否                                                                                                            |
| 是-單一值       | 否                                                                                                            |
| 已編制索引             | 否                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8070                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





