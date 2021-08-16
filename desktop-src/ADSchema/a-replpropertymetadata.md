---
title: 複寫-屬性中繼資料屬性
description: 追蹤 DS 物件的內部複寫狀態資訊。 您可以透過公用 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。 存在於所有 DS 物件上。
ms.assetid: 5776208c-8138-4b0a-855a-8bddcbd2e532
ms.tgt_platform: multiple
keywords:
- 複寫-屬性-中繼資料屬性 AD 架構
- replPropertyMetaData 屬性 AD 架構
topic_type:
- apiref
api_name:
- Repl-Property-Meta-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dedebf88923d64ba14882a885f74254474664e79756dd7f12fd2e3b02a09545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117836660"
---
# <a name="repl-property-meta-data-attribute"></a>複寫-屬性中繼資料屬性

追蹤 DS 物件的內部複寫狀態資訊。 您可以透過公用 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。 存在於所有 DS 物件上。



| 進入 | 值 |
|-------------------|------------------------------------------------------------------------------|
| CN                | 複寫-屬性中繼資料                                                      |
| Ldap-顯示名稱 | replPropertyMetaData                                                         |
| 大小              | 長度與物件上可複製屬性的數目成正比。 |
| 更新許可權  | 此值是由系統所設定。                                             |
| 更新頻率  | 變更，以回應物件中的任何複寫變更。                |
| Attribute-Id      | 1.2.840.113556.1.4.3                                                         |
| 系統識別碼-Guid    | 281416c0-1968-11d0-a28f-00aa003049e2                                         |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                        |



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
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000013                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x0000001B                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



 

 





