---
title: UpToDate-Vector 屬性
description: 追蹤整個 NC 的內部複寫狀態資訊。 您可以透過 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。 存在於所有 NC 根物件上。
ms.assetid: f23d94f8-c31b-447f-98c3-c35a4f5f1d43
ms.tgt_platform: multiple
keywords:
- 複寫-UpToDate-向量屬性 AD 架構
- replUpToDateVector 屬性 AD 架構
topic_type:
- apiref
api_name:
- Repl-UpToDate-Vector
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 413291da92f52e0e6241e6dcfb6ca50303ed5740d370b1f5f900904266a75446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423729"
---
# <a name="repl-uptodate-vector-attribute"></a>UpToDate-Vector 屬性

追蹤整個 NC 的內部複寫狀態資訊。 您可以透過 API DsReplicaGetInfo () ，以公用形式解壓縮這裡的資訊。 存在於所有 NC 根物件上。



| 進入 | 值 |
|-------------------|--------------------------------------------------------------------------------|
| CN                | 複寫-UpToDate-向量                                                           |
| Ldap-顯示名稱 | replUpToDateVector                                                             |
| 大小              | 長度與 NC 的 (過去和目前) 的複本數目成正比。 |
| 更新許可權  | 此值是由系統所設定。                                               |
| 更新頻率  | 回應已完成的輸入複寫週期的變更。                   |
| Attribute-Id      | 1.2.840.113556.1.4.4                                                           |
| 系統識別碼-Guid    | bf967a16-0de6-11d0-a285-00aa003049e2                                           |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                          |



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
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000013                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



 

 





