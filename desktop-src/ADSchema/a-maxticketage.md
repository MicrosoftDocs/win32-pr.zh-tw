---
title: 最大票證-存留期屬性
description: 這個屬性會決定使用者的票證授與票證 (TGT) 可用於 Kerberos 驗證的最大時間量（以小時為單位）。
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- 最大票證-存留期屬性 AD 架構
- maxTicketAge 屬性 AD 架構
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c876bbab2b60d655464129d0a59aeda110f78d8e2514866a3bcf28a859cb3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301008"
---
# <a name="max-ticket-age-attribute"></a>最大票證-存留期屬性

這個屬性會決定使用者的票證授與票證 (TGT) 可用於 Kerberos 驗證的最大時間量（以小時為單位）。 當使用者的 TGT 過期時，必須要求新的 TGT，或必須更新現有的 TGT。 根據預設，在預設網域群組原則物件 (GPO) 中，此設定為10小時。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | 最大票證-存留期                       |
| Ldap-顯示名稱 | maxTicketAge                         |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| 系統識別碼-Guid    | bf9679be-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|----------------------------------------------------|
| 連結識別碼                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | 否                                              |
| 是-單一值       | 是                                               |
| 已編制索引             | 否                                              |
| 在通用類別目錄中      | 否                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------------|
| 連結識別碼                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | 否                                              |
| 是-單一值       | 是                                               |
| 已編制索引             | 否                                              |
| 在通用類別目錄中      | 否                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------|
| 連結識別碼                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | 否                                              |
| 是-單一值       | 是                                               |
| 已編制索引             | 否                                              |
| 在通用類別目錄中      | 否                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------|
| 連結識別碼                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | 否                                              |
| 是-單一值       | 是                                               |
| 已編制索引             | 否                                              |
| 在通用類別目錄中      | 否                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------|
| 連結識別碼                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | 否                                              |
| 是-單一值       | 是                                               |
| 已編制索引             | 否                                              |
| 在通用類別目錄中      | 否                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------|
| 連結識別碼                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | 否                                              |
| 是-單一值       | 是                                               |
| 已編制索引             | 否                                              |
| 在通用類別目錄中      | 否                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> |



 

 





