---
title: SAM-Account-Name 屬性
description: 用來支援執行舊版作業系統之用戶端和伺服器的登入名稱，例如 Windows NT 4.0、Windows 95、Windows 98 和 LAN Manager。
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- SAM-帳戶-名稱屬性 AD 架構
- sAMAccountName 屬性 AD 架構
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74aa558f63c2e1822f1435cdafd6290755b92b4d5e34c329d8472693f37185d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022226"
---
# <a name="sam-account-name-attribute"></a>SAM-Account-Name 屬性

用來支援執行舊版作業系統之用戶端和伺服器的登入名稱，例如 Windows NT 4.0、Windows 95、Windows 98 和 LAN Manager。

這個屬性必須是20個字元以上，才能支援較早的用戶端，而且不能包含下列任何字元：

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| 進入 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | SAM-帳戶-名稱                                                                         |
| Ldap-顯示名稱 | sAMAccountName                                                                           |
| 大小              | 20個字元或更少。                                                                   |
| 更新許可權  | 網域系統管理員                                                                     |
| 更新頻率  | 建立客戶紀錄時，應該指派此值，而且不應該變更。 |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| 系統識別碼-Guid    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                              |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 是                                                         |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 是                                                         |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 是                                                         |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 是                                                         |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 是                                                         |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 是                                                         |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



 

 





