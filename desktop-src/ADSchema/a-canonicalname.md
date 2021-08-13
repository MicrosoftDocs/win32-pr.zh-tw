---
title: Canonical-Name 屬性
description: 標準格式的物件名稱。
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Canonical-Name 屬性 AD 架構
- canonicalName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d88b31dd351e255c252188388bd1ba06b3a1c073163f5cd2cc9d2deac16a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307188"
---
# <a name="canonical-name-attribute"></a>Canonical-Name 屬性

標準格式的物件名稱。 myserver2.fabrikam.com/users/jeffsmith 是標準格式的辨別名稱範例。 這是一個結構化屬性。 傳回的結果與下列 Active Directory 函數所傳回的結果相同： DsCrackNames (Null、DS \_ 名稱 \_ 旗標 \_ \_ 僅限語法、ds \_ FQDN \_ 1779 \_ 名稱、ds 正式 \_ \_ 名稱、... ) 。

如需有關名稱格式的詳細資訊，請參閱 [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa)。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | Canonical-Name                              |
| Ldap-顯示名稱 | canonicalName                               |
| 大小              | \-                                          |
| 更新許可權  | \-                                          |
| 更新頻率  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.916                      |
| 系統識別碼-Guid    | 9a7ad945-ca53-11d1-bbd0-0080c76670c0        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



 

