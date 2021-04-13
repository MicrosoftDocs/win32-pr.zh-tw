---
title: MSMQ 保護的-來源屬性
description: 這是 MSMQ 物件的一部分，它是透過呼叫 API 至 MQCreateQueue 或 MQSetProperties 來設定的。 它會控制 MSMQ 是否只接受來自安全來源的訊息 (例如，此佇列的 HTTPs) 。
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- MSMQ 保護-來源屬性 AD 架構
- MSMQ-SecuredSource 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509604"
---
# <a name="msmq-secured-source-attribute"></a>MSMQ 保護的-來源屬性

這是 MSMQ 物件的一部分，它是透過呼叫 API 至 MQCreateQueue 或 MQSetProperties 來設定的。 它會控制 MSMQ 是否只接受來自安全來源的訊息 (例如，此佇列的 HTTPs) 。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | MSMQ 安全-來源                  |
| Ldap-顯示名稱 | MSMQ-SecuredSource                   |
| 大小              | 4 個位元組                              |
| 更新許可權  | 佇列擁有者。                     |
| 更新頻率  | 當佇列建立時。             |
| Attribute-Id      | 1.2.840.113556.1.4.1713              |
| 系統識別碼-Guid    | 8bf0221b-7a06-4d63-91f0-1499941813d3 |
| Syntax            | [**Boolean**](s-boolean.md)         |



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
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 對                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**MSMQ-佇列**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 對                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**MSMQ-佇列**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 對                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**MSMQ-佇列**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 對                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**MSMQ-佇列**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 對                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**MSMQ-佇列**](c-msmqqueue.md)<br/> |



 

 





