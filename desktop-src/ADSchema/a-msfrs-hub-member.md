---
title: ms-FRS-Hub 成員屬性
description: Ms-chap 中樞成員屬性是用來記錄慣用的 NTFRS 拓撲設定。
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- ms-FRS-中樞-成員屬性 AD 架構
- msFRS-中樞-成員屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa08d1eb3cbb8086149192e6ecd5fa3880f01e6cfa1800468d2825c243b211e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803307"
---
# <a name="ms-frs-hub-member-attribute"></a>ms-FRS-Hub 成員屬性

**Ms-chap 中樞成員** 屬性是用來記錄慣用的 NTFRS 拓撲設定。 將 FRS 成員新增或刪除至複本集時，會參考這些屬性，並對複本集中的其他 FRS 成員之間的連接進行適當的調整。



| 進入 | 值 |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-中樞成員                                                  |
| Ldap-顯示名稱 | msFRS-中樞-成員                                                   |
| 大小              | \-                                                                 |
| 更新許可權  | 網域系統管理員                                               |
| 更新頻率  | 建立複本集或偏好的拓撲變更時。 |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| 系統識別碼-Guid    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------------------------------|
| 連結識別碼                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 是                                                      |
| 已編制索引             | 否                                                     |
| 在通用類別目錄中      | 否                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| 中使用的類別        | [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------|
| 連結識別碼                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 是                                                      |
| 已編制索引             | 否                                                     |
| 在通用類別目錄中      | 否                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| 中使用的類別        | [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------------------------------|
| 連結識別碼                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 是                                                      |
| 已編制索引             | 否                                                     |
| 在通用類別目錄中      | 否                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| 中使用的類別        | [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------|
| 連結識別碼                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 是                                                      |
| 已編制索引             | 否                                                     |
| 在通用類別目錄中      | 否                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| 中使用的類別        | [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------------------------------|
| 連結識別碼                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 是                                                      |
| 已編制索引             | 否                                                     |
| 在通用類別目錄中      | 否                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| 中使用的類別        | [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>備註

這是 [**NTFRS 成員**](c-ntfrsmember.md) 物件的完整分辨名稱。 辨別名稱的格式為 "CN = *<computerGuid>* ，cn = *<Dfs Link Name>* ，cn = *<Dfs Root name>* ，Cn = DFS 磁片區，Cn = File REPLICATION Service，cn = System，DC = ..."

 

 





