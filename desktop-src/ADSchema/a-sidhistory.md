---
title: SID-History 屬性
description: 如果物件是從另一個網域移出，則包含用於物件的先前 Sid。
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- SID-History 屬性 AD 架構
- sIDHistory 屬性 AD 架構
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c2dbfb3572392bdbed3f13683adc1cbf64b70e061962975a178f8380f55f5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836288"
---
# <a name="sid-history-attribute"></a>SID-History 屬性

如果物件是從另一個網域移出，則包含用於物件的先前 Sid。 每當物件從一個網域移到另一個網域時，就會建立新的 SID，而新的 SID 就會變成 objectSID。 先前的 SID 會新增至 sIDHistory 屬性。



| 進入 | 值 |
|-------------------|------------------------------------------------|
| CN                | SID-History                                    |
| Ldap-顯示名稱 | sIDHistory                                     |
| 大小              | \-                                             |
| 更新許可權  | 此值是由系統所設定。               |
| 更新頻率  | 每次物件移至新的網域時。 |
| Attribute-Id      | 1.2.840.113556.1.4.609                         |
| 系統識別碼-Guid    | 17eb4278-d167-11d0-b002-0000f80367c1           |
| Syntax            | [**(Sid) 的字串**](s-string-sid.md)            |



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
| System-Only            | 是                                                         |
| 是-單一值       | 否                                                        |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 是                                                         |
| 在通用類別目錄中      | 是                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



 

 





