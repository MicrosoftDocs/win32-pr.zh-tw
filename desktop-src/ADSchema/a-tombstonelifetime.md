---
title: Tombstone-Lifetime 屬性
description: 從目錄服務移除已刪除物件之前的天數。
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Tombstone-Lifetime 屬性 AD 架構
- tombstoneLifetime 屬性 AD 架構
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845279"
---
# <a name="tombstone-lifetime-attribute"></a>Tombstone-Lifetime 屬性

從目錄服務移除已刪除物件之前的天數。 這有助於從複寫的伺服器中移除物件，並防止還原重新介紹基於已刪除的物件。 此值位於 configuration NIC 的目錄服務物件中。



| 進入 | 值 |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| Ldap-顯示名稱 | tombstoneLifetime                                         |
| 大小              | 4個位元組。 未輸入任何值時，預設值為60天。 |
| 更新許可權  | \-                                                        |
| 更新頻率  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| 系統識別碼-Guid    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Syntax            | [**列舉型別**](s-enumeration.md)                      |



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
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | 否                                            |
| 是-單一值       | 對                                             |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | 否                                            |
| 是-單一值       | 對                                             |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | 否                                            |
| 是-單一值       | 對                                             |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | 否                                            |
| 是-單一值       | 對                                             |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | 否                                            |
| 是-單一值       | 對                                             |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | 否                                            |
| 是-單一值       | 對                                             |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | 否                                            |
| 是-單一值       | 對                                             |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



 

 





