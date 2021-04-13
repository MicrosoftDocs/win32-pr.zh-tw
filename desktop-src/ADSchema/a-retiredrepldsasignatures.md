---
title: 已淘汰-複寫-DSA-簽章屬性
description: 追蹤指定 DC 的過去 DS 複寫身分識別。
ms.assetid: 82e8b222-5635-41ad-b2ab-386c9e6aa280
ms.tgt_platform: multiple
keywords:
- 已淘汰-複寫-DSA-簽章屬性 AD 架構
- retiredReplDSASignatures 屬性 AD 架構
topic_type:
- apiref
api_name:
- Retired-Repl-DSA-Signatures
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9a4cb4030a8d3aa24244bc2e7a2702e83686fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385430"
---
# <a name="retired-repl-dsa-signatures-attribute"></a>已淘汰-複寫-DSA-簽章屬性

追蹤指定 DC 的過去 DS 複寫身分識別。



| 進入 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| CN                | 已淘汰-複寫-DSA-簽章                                                         |
| Ldap-顯示名稱 | retiredReplDSASignatures                                                            |
| 大小              | 長度與從備份還原 DC 的次數成正比。 |
| 更新許可權  | 此值是由系統所設定。                                                    |
| 更新頻率  | \-                                                                                  |
| Attribute-Id      | 1.2.840.113556.1.4.673                                                              |
| 系統識別碼-Guid    | 7bfdcb7f-4807-11d1-a9c3-0000f80367c1                                                |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                               |



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
|------------------------|------------------------------------------|
| 連結識別碼                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | 對                                     |
| 是-單一值       | 對                                     |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | 對                                     |
| 是-單一值       | 對                                     |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | 對                                     |
| 是-單一值       | 對                                     |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | 對                                     |
| 是-單一值       | 對                                     |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | 對                                     |
| 是-單一值       | 對                                     |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | 對                                     |
| 是-單一值       | 對                                     |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | 對                                     |
| 是-單一值       | 對                                     |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





