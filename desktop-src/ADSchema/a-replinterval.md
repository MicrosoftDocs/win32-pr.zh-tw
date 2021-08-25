---
title: Repl-Interval 屬性
description: Site-Link 物件的屬性，可定義網站清單中網站之間的複寫間隔（以分鐘為單位）。
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Repl-Interval 屬性 AD 架構
- replInterval 屬性 AD 架構
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5cd02d3458684f6d70cff84435c7809fcd4c912befd65373a264f961cefd72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837438"
---
# <a name="repl-interval-attribute"></a>Repl-Interval 屬性

Site-Link 物件的屬性，可定義網站清單中網站之間的複寫間隔（以分鐘為單位）。 必須是15分鐘的倍數 (跨網站 DS 複寫) 的細微性、最少15分鐘，以及最多10080分鐘 (一周) 。



| 進入 | 值 |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| Ldap-顯示名稱 | replInterval                                   |
| 大小              | 4 個位元組                                        |
| 更新許可權  | 企業系統管理員                       |
| 更新頻率  | 當複寫間隔需要變更時。 |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| 系統識別碼-Guid    | 45ba9d1a-56fa-11d2-90d0-00c04fd91ab1           |
| Syntax            | [**列舉型別**](s-enumeration.md)           |



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
|------------------------|------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | 否                                                                                                      |
| 是-單一值       | 是                                                                                                       |
| 已編制索引             | 否                                                                                                      |
| 在通用類別目錄中      | 否                                                                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| 中使用的類別        | [**站間-傳輸**](c-intersitetransport.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | 否                                                                                                      |
| 是-單一值       | 是                                                                                                       |
| 已編制索引             | 否                                                                                                      |
| 在通用類別目錄中      | 否                                                                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| 中使用的類別        | [**站間-傳輸**](c-intersitetransport.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | 否                                                                                                      |
| 是-單一值       | 是                                                                                                       |
| 已編制索引             | 否                                                                                                      |
| 在通用類別目錄中      | 否                                                                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| 中使用的類別        | [**站間-傳輸**](c-intersitetransport.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | 否                                                                                                      |
| 是-單一值       | 是                                                                                                       |
| 已編制索引             | 否                                                                                                      |
| 在通用類別目錄中      | 否                                                                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| 中使用的類別        | [**站間-傳輸**](c-intersitetransport.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | 否                                                                                                      |
| 是-單一值       | 是                                                                                                       |
| 已編制索引             | 否                                                                                                      |
| 在通用類別目錄中      | 否                                                                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| 中使用的類別        | [**站間-傳輸**](c-intersitetransport.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | 否                                                                                                      |
| 是-單一值       | 是                                                                                                       |
| 已編制索引             | 否                                                                                                      |
| 在通用類別目錄中      | 否                                                                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| 中使用的類別        | [**站間-傳輸**](c-intersitetransport.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | 否                                                                                                      |
| 是-單一值       | 是                                                                                                       |
| 已編制索引             | 否                                                                                                      |
| 在通用類別目錄中      | 否                                                                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| 中使用的類別        | [**站間-傳輸**](c-intersitetransport.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



 

 





