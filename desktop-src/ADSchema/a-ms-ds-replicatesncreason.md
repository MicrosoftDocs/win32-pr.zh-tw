---
title: MS-DS-複寫-NC-Reason 屬性
description: NtdsConnection 物件的屬性，指出 (或) KCC 顯示連接在複寫拓撲中是否有用。 是多重值，而且具有 DistName + 二進位語法，其中二進位部分是 int 大小的位。
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- MS-DS-複寫-NC-原因屬性 AD 架構
- ReplicatesNCReason 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385338"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>MS-DS-複寫-NC-Reason 屬性

NtdsConnection 物件的屬性，指出 (或) KCC 顯示連接在複寫拓撲中是否有用。 是多重值，而且具有 DistName + 二進位語法，其中二進位部分是 int 大小的位。



| 進入 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-複寫-NC-原因                                                                                                                 |
| Ldap-顯示名稱 | ReplicatesNCReason                                                                                                                   |
| 大小              | 二進位部分的值： 0 = 否 \_ 原因，1 = GC \_ 拓撲，2 = 環形 \_ 拓撲，4 = 將 \_ 躍點拓撲降至最低 \_ ，8 = 過時 \_ 伺服器 \_ 拓撲。 |
| 更新許可權  | 此值是由系統所設定。                                                                                                           |
| 更新頻率  | 可以變更以回應網路拓撲中的變更。                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| 系統識別碼-Guid    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|--------------------------------------------------------|
| 連結識別碼                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | 否                                                  |
| 是-單一值       | 否                                                  |
| 已編制索引             | 否                                                  |
| 在通用類別目錄中      | 否                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------------|
| 連結識別碼                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | 否                                                  |
| 是-單一值       | 否                                                  |
| 已編制索引             | 否                                                  |
| 在通用類別目錄中      | 否                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|--------------------------------------------------------|
| 連結識別碼                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | 否                                                  |
| 是-單一值       | 否                                                  |
| 已編制索引             | 否                                                  |
| 在通用類別目錄中      | 否                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------|
| 連結識別碼                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | 否                                                  |
| 是-單一值       | 否                                                  |
| 已編制索引             | 否                                                  |
| 在通用類別目錄中      | 否                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------------------|
| 連結識別碼                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | 否                                                  |
| 是-單一值       | 否                                                  |
| 已編制索引             | 否                                                  |
| 在通用類別目錄中      | 否                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------|
| 連結識別碼                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | 否                                                  |
| 是-單一值       | 否                                                  |
| 已編制索引             | 否                                                  |
| 在通用類別目錄中      | 否                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------------|
| 連結識別碼                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | 否                                                  |
| 是-單一值       | 否                                                  |
| 已編制索引             | 否                                                  |
| 在通用類別目錄中      | 否                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> |



 

 





