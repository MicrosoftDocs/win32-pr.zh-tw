---
title: ms-DS-信任-樹系信任資訊屬性
description: 包含樹系信任資訊 (系統用於 Trusted-Domain 物件的二進位 BLOB) 。
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- ms-DS-信任-樹系信任資訊屬性 AD 架構
- TrustForestTrustInfo 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae350001aa616052c1f0358497364ecfbce55d40e91314c56100d12848efc0ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960567"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a>ms-DS-信任-樹系信任資訊屬性

包含樹系信任資訊 (系統用於 Trusted-Domain 物件的二進位 BLOB) 。



| 進入 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-信任-樹系信任資訊                                                                                      |
| Ldap-顯示名稱 | TrustForestTrustInfo                                                                                          |
| 大小              | \-                                                                                                                 |
| 更新許可權  | \-                                                                                                                 |
| 更新頻率  | 只有在樹系之間的信任關係變更時才會發生。 如果信任樹系的拓撲變更，就會發生這種情況。 |
| Attribute-Id      | 1.2.840.113556.1.4.1702                                                                                            |
| 系統識別碼-Guid    | 29cc866e-49d3-4969-942e-1dbc0925d183                                                                               |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                              |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
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
| 是-單一值       | 是                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 是                                                 |
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
| 是-單一值       | 是                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 是                                                 |
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
| 是-單一值       | 是                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 是                                                 |
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
| 是-單一值       | 是                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 是                                                 |
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
| 是-單一值       | 是                                                 |
| 已編制索引             | 否                                                |
| 在通用類別目錄中      | 是                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> |



 

 





