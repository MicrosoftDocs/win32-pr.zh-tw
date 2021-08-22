---
title: ms DS-登入時間同步處理間隔屬性
description: 這個屬性會控制使用者或電腦上次登入時間（記錄在 lastLogonTimestamp 屬性中）複寫到網域中所有 Dc 的資料細微性（以天為單位）。
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- ms DS-登入時間-同步處理間隔屬性 AD 架構
- LogonTimeSyncInterval 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa27a1d6281eda7eea9f88a11c4ca6632422a1cfd9f0cb471aab513018c56150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118684632"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a>ms DS-登入時間同步處理間隔屬性

這個屬性會控制使用者或電腦上次登入時間（記錄在 lastLogonTimestamp 屬性中）複寫到網域中所有 Dc 的資料細微性（以天為單位）。



| 進入 | 值 |
|-------------------|------------------------------------------------------------------------------------------------------------|
| CN                | ms DS-登入時間-同步處理間隔                                                                             |
| Ldap-顯示名稱 | LogonTimeSyncInterval                                                                                 |
| 大小              | 4 個位元組                                                                                                    |
| 更新許可權  | 網域系統管理員                                                                                       |
| 更新頻率  | 這很少是因為這是一項原則設定，只有在需要全網域原則的變更時才會更新。 |
| Attribute-Id      | 1.2.840.113556.1.4.1784                                                                                    |
| 系統識別碼-Guid    | ad7940f8-e43a-4a42-83bc-d688e59ea605                                                                       |
| Syntax            | [**列舉型別**](s-enumeration.md)                                                                       |



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



 

 





