---
title: Trust-Attributes 屬性
description: 這個屬性會儲存受信任網域的信任屬性。
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Trust-Attributes 屬性 AD 架構
- trustAttributes 屬性 AD 架構
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687119"
---
# <a name="trust-attributes-attribute"></a>Trust-Attributes 屬性

這個屬性會儲存受信任網域的信任屬性。 可能的屬性值如下所示：

-   信任 \_ 屬性 \_ 非可 \_ 轉移停用轉移。
-   信任 \_ 屬性 \_ 樹狀目錄 \_ 父系信任設定為組織樹狀目錄父系。
-   信任 \_ 屬性 \_ 樹狀結構 \_ 根信任設定為樹系中的另一個樹狀目錄根。
-   信任 \_ 屬性 \_ 僅 \_ 限上層僅限上層用戶端的受信任連結有效。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| Ldap-顯示名稱 | trustAttributes                      |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| 系統識別碼-Guid    | 80a67e5a-9f22-11d0-afdd-00c04fd930c9 |
| Syntax            | [**列舉型別**](s-enumeration.md) |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 否                                                |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 對                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 對                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 對                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 對                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------|
| 連結識別碼                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | 否                                                |
| 是-單一值       | 對                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 對                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



 

 





