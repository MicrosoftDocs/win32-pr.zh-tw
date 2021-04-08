---
title: ms-FRS-拓撲-Pref 屬性
description: Pref 屬性是用來記錄慣用的 NTFRS 拓撲設定。
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- ms-chap-拓撲-Pref 屬性 AD 架構
- msFRS-拓撲-Pref 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687011"
---
# <a name="ms-frs-topology-pref-attribute"></a>ms-FRS-拓撲-Pref 屬性

**Pref** 屬性是用來記錄慣用的 NTFRS 拓撲設定。 將 FRS 成員新增或刪除至複本集時，會參考這些屬性，並在複本集中的其他 FRS 成員之間進行的連接調整。

這個屬性的有效值如下所示。

| 值 | 描述                              |
|-------|------------------------------------------|
| 1     | FRS \_ RSTOPOLOGYPREF \_ 環形<br/>     |
| 2     | FRS \_ RSTOPOLOGYPREF \_ >PEER-HUBSPOKE<br/> |
| 3     | FRS \_ RSTOPOLOGYPREF \_ FULLMESH<br/> |
| 4     | FRS \_ RSTOPOLOGYPREF \_ 自訂<br/>   |



 



| 進入 | 值 |
|-------------------|--------------------------------------------------------------------|
| CN                | 毫秒-FRS-拓撲-Pref                                               |
| Ldap-顯示名稱 | msFRS-拓撲-Pref                                                |
| 大小              | \-                                                                 |
| 更新許可權  | 網域系統管理員                                               |
| 更新頻率  | 建立複本集或偏好的拓撲變更時。 |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| 系統識別碼-Guid    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                        |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------------------------------|
| 連結識別碼                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 對                                                      |
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
| 連結識別碼                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 對                                                      |
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
| 連結識別碼                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 對                                                      |
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
| 連結識別碼                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 對                                                      |
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
| 連結識別碼                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | 否                                                     |
| 是-單一值       | 對                                                      |
| 已編制索引             | 否                                                     |
| 在通用類別目錄中      | 否                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| 中使用的類別        | [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> |



 

 





