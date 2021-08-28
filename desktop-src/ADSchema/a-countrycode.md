---
title: Country-Code 屬性
description: 指定使用者選擇之語言的國家/地區代碼。 Windows 2000 不會使用這個值。
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Country-Code 屬性 AD 架構
- countryCode 屬性 AD 架構
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7843a2724043e504538ad6388e92dfc205463e76e082c266b5ee1f4f095207ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961777"
---
# <a name="country-code-attribute"></a>Country-Code 屬性

指定使用者選擇之語言的國家/地區代碼。 Windows 2000 不會使用這個值。



| 進入 | 值 |
|-------------------|-----------------------------------------|
| CN                | Country-Code                            |
| Ldap-顯示名稱 | countryCode                             |
| 大小              | 2 個位元組                                 |
| 更新許可權  | 帳戶擁有者或網域系統管理員   |
| 更新頻率  | 當使用者的國家/地區變更時。 |
| Attribute-Id      | 1.2.840.113556.1.4.25                   |
| 系統識別碼-Guid    | 5fd42471-1262-11d0-a060-00aa006c33ed    |
| Syntax            | [**列舉型別**](s-enumeration.md)    |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | 否                                                                                                                             |
| 是-單一值       | 是                                                                                                                              |
| 已編制索引             | 否                                                                                                                             |
| 在通用類別目錄中      | 否                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                      |
| Range-Lower            | \-                                                                                                                                |
| Range-Upper            | \-                                                                                                                                |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | 否                                                                                                                             |
| 是-單一值       | 是                                                                                                                              |
| 已編制索引             | 否                                                                                                                             |
| 在通用類別目錄中      | 否                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|----------------------------------------------------------------|
| 連結識別碼                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | 否                                                          |
| 是-單一值       | 是                                                           |
| 已編制索引             | 否                                                          |
| 在通用類別目錄中      | 否                                                          |
| NT-Security-描述元 | O:BAG：不正確： S：                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 65535                                                          |
| Search-Flags           | 0x00000010                                                     |
| System-Flags           | 0x00000010                                                     |
| 中使用的類別        | [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | 否                                                                                                                             |
| 是-單一值       | 是                                                                                                                              |
| 已編制索引             | 否                                                                                                                             |
| 在通用類別目錄中      | 否                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | 否                                                                                                                             |
| 是-單一值       | 是                                                                                                                              |
| 已編制索引             | 否                                                                                                                             |
| 在通用類別目錄中      | 否                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | 否                                                                                                                             |
| 是-單一值       | 是                                                                                                                              |
| 已編制索引             | 否                                                                                                                             |
| 在通用類別目錄中      | 否                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | 否                                                                                                                             |
| 是-單一值       | 是                                                                                                                              |
| 已編制索引             | 否                                                                                                                             |
| 在通用類別目錄中      | 否                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



 

 





