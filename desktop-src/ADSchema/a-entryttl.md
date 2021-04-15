---
title: 專案-TTL 屬性
description: 此操作屬性是由伺服器維護，並且似乎出現在每個動態專案中。
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- 專案-TTL 屬性 AD 架構
- entryTTL 屬性 AD 架構
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467188"
---
# <a name="entry-ttl-attribute"></a>專案-TTL 屬性

此操作屬性是由伺服器維護，並且似乎出現在每個動態專案中。 當專案不包含 dynamicObject 物件類別時，屬性不會出現。 這個屬性的值是以秒為單位的時間，此專案會在從目錄中消失之前繼續存在。 如果沒有中間的「重新整理」作業，則在兩個連續搜尋中讀取屬性所傳回的值一定會 nonincreasing。 允許的最小值為0，表示專案可能會消失而不發出警告。 屬性標示為無使用者修改，因為它只能使用重新整理作業來變更。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | 專案-TTL                                   |
| Ldap-顯示名稱 | entryTTL                                    |
| 大小              | 4個位元組。 最大值 = 1 年，預設值 = 1 天。 |
| 更新許可權  | \-                                          |
| 更新頻率  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| 系統識別碼-Guid    | d213decc-d81a-4384-aac2-dcfcfd631cf8        |
| Syntax            | [**列舉型別**](s-enumeration.md)        |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| 中使用的類別        | [**動態物件**](c-dynamicobject.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| 中使用的類別        | [**動態物件**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| 中使用的類別        | [**動態物件**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| 中使用的類別        | [**動態物件**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| 中使用的類別        | [**動態物件**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| 中使用的類別        | [**動態物件**](c-dynamicobject.md)<br/> |



 

 





