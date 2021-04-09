---
title: RID-先前組態集區屬性
description: 包含網域控制站所配置的 (Rid) 的相對識別碼集區。
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-先前組態集區屬性 AD 架構
- rIDPreviousAllocationPool 屬性 AD 架構
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844939"
---
# <a name="rid-previous-allocation-pool-attribute"></a>RID-先前組態集區屬性

**Rid-Previous 組態集** 區屬性包含網域控制站所配置的 (rid) 的相對識別碼集區。 這個屬性是八位元組的值，其中包含一組四個位元組的整數，表示 RID 集區的開始和結束值。 開始值是在四個位元組的下方，而結束值是在四個位元組內。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | RID-先前組態集區         |
| Ldap-顯示名稱 | rIDPreviousAllocationPool            |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| 系統識別碼-Guid    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
| Syntax            | [**間隔**](s-interval.md)       |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|----------------------------------------|
| 連結識別碼                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | 對                                   |
| 是-單一值       | 對                                   |
| 已編制索引             | 否                                  |
| 在通用類別目錄中      | 否                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| 中使用的類別        | [**RID 集**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------|
| 連結識別碼                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | 對                                   |
| 是-單一值       | 對                                   |
| 已編制索引             | 否                                  |
| 在通用類別目錄中      | 否                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| 中使用的類別        | [**RID 集**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------|
| 連結識別碼                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | 對                                   |
| 是-單一值       | 對                                   |
| 已編制索引             | 否                                  |
| 在通用類別目錄中      | 否                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| 中使用的類別        | [**RID 集**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------|
| 連結識別碼                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | 對                                   |
| 是-單一值       | 對                                   |
| 已編制索引             | 否                                  |
| 在通用類別目錄中      | 否                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| 中使用的類別        | [**RID 集**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------|
| 連結識別碼                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | 對                                   |
| 是-單一值       | 對                                   |
| 已編制索引             | 否                                  |
| 在通用類別目錄中      | 否                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| 中使用的類別        | [**RID 集**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------|
| 連結識別碼                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | 對                                   |
| 是-單一值       | 對                                   |
| 已編制索引             | 否                                  |
| 在通用類別目錄中      | 否                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| 中使用的類別        | [**RID 集**](c-ridset.md)<br/> |



 

 





