---
title: MSMQ-多播-位址屬性
description: 這是 MSMQ 物件的一部分，它是透過呼叫 API 至 MQCreateQueue 或 MQSetProperties 來設定的。 它會控制 MSMQ 是否接受來自多播位址的訊息。
ms.assetid: 65622cc9-81d9-42c6-b208-cac703f32244
ms.tgt_platform: multiple
keywords:
- MSMQ-多播-位址屬性 AD 架構
- MSMQ-MulticastAddress 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Multicast-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ad4deca3f742dc072f7a83363b608c1c470f50fca1626793c59b13e91fcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762738"
---
# <a name="msmq-multicast-address-attribute"></a>MSMQ-多播-位址屬性

這是 MSMQ 物件的一部分，它是透過呼叫 API 至 MQCreateQueue 或 MQSetProperties 來設定的。 它會控制 MSMQ 是否接受來自多播位址的訊息。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | MSMQ-多播-位址                      |
| Ldap-顯示名稱 | MSMQ-MulticastAddress                       |
| 大小              | 4 個位元組                                     |
| 更新許可權  | 佇列擁有者。                            |
| 更新頻率  | 當佇列建立時。                    |
| Attribute-Id      | 1.2.840.113556.1.4.1714                     |
| 系統識別碼-Guid    | 1d2f4412-f10d-4337-9b48-6e5b125cd265        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
| 在通用類別目錄中      | 是                                         |
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
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 是                                         |
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
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 是                                         |
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
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 是                                         |
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
| 是-單一值       | 是                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 是                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**MSMQ-佇列**](c-msmqqueue.md)<br/> |



 

 





