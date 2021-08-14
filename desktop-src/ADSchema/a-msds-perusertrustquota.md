---
title: 每一使用者的 MS-信任配額屬性
description: 用來強制執行每個使用者的配額，以建立新的 control 存取權限所授權的 Trusted-Domain 物件，建立--------------樹系信任。
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- 每一使用者的 MS DS-信任配額屬性 AD 架構
- PerUserTrustQuota 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fc51a6e3e3e9f3d14534487590985197ed7c97fbca8bc1042108bfcdba97530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425824"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a>每一使用者的 MS-信任配額屬性

用來強制執行每個使用者的配額，以建立新的 control 存取權限所授權的 Trusted-Domain 物件，建立--------------樹系信任。 這個屬性會限制單一非系統管理員使用者可以建立的 Trusted-Domain 物件數目。



| 進入 | 值 |
|-------------------|-------------------------------------------|
| CN                | 每一使用者的 MS-信任-配額                |
| Ldap-顯示名稱 | PerUserTrustQuota                    |
| 大小              | \-                                        |
| 更新許可權  | 網域系統管理員                      |
| 更新頻率  | 在建立樹系時，很少發生。 |
| Attribute-Id      | 1.2.840.113556.1.4.1788                   |
| 系統識別碼-Guid    | d161adf0-ca24-4993-a3aa-8b2c981302e8      |
| Syntax            | [**列舉型別**](s-enumeration.md)      |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**Sam-網域**](c-samdomain.md)<br/> |



 

 





