---
title: X121-Address 屬性
description: 物件的 * 121 位址。
ms.assetid: 3fe3cb04-6a76-4b5b-af4e-c73afd7e0412
ms.tgt_platform: multiple
keywords:
- X121-Address 屬性 AD 架構
- x121Address 屬性 AD 架構
topic_type:
- apiref
api_name:
- X121-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c16831af773869649ed663ebef34e70d9a9e8f4ed329fa14bc41938a253f16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959937"
---
# <a name="x121-address-attribute"></a>X121-Address 屬性

物件的 * 121 位址。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | X121-Address                                |
| Ldap-顯示名稱 | x121Address                                 |
| 大小              | 15個位元組                                    |
| 更新許可權  | \-                                          |
| 更新頻率  | \-                                          |
| Attribute-Id      | 2.5.4.24                                    |
| 系統識別碼-Guid    | bf967a7b-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Numeric)**](s-string-numeric.md) |



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
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                          |
| System-Only            | 否                                                                                                                                                                                                                                                                                                           |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                           |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                               |
| MAPI-Id                | 0x8158                                                                                                           |
| System-Only            | 否                                                                                                            |
| 是-單一值       | 否                                                                                                            |
| 已編制索引             | 否                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 15                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                   |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| 中使用的類別        | [**組織**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織角色**](c-organizationalrole.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> [**居住人**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





