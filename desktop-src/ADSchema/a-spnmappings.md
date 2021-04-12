---
title: SPN-Mappings 屬性
description: 這個多重值屬性包含服務主體名稱的清單 (SPN) 來顯示 SPN 類型的等價。
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- SPN-Mappings 屬性 AD 架構
- sPNMappings 屬性 AD 架構
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509658"
---
# <a name="spn-mappings-attribute"></a>SPN-Mappings 屬性

這個多重值屬性包含服務主體名稱的清單 (SPN) 來顯示 SPN 類型的等價。 SPN 是用戶端用來唯一識別服務實例的名稱。 若您透過樹系在電腦上安裝多個服務執行個體，則每個執行個體都須有自己的 SPN。 若用戶端需使用多個名稱進行驗證，則指定的服務執行個體可擁有多個 SPN。 例如，"ldap/..."Spn 可以對應，使其相當於「主機/...」Spn。



| 進入 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| Ldap-顯示名稱 | sPNMappings                                                                                                        |
| 大小              | \-                                                                                                                 |
| 更新許可權  | 此值會在產品安裝期間設定。 系統管理員可以在稍後修改它。 |
| 更新頻率  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| 系統識別碼-Guid    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                        |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | 否                                            |
| 是-單一值       | 否                                            |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | 否                                            |
| 是-單一值       | 否                                            |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | 否                                            |
| 是-單一值       | 否                                            |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | 否                                            |
| 是-單一值       | 否                                            |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | 否                                            |
| 是-單一值       | 否                                            |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------|
| 連結識別碼                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | 否                                            |
| 是-單一值       | 否                                            |
| 已編制索引             | 否                                            |
| 在通用類別目錄中      | 否                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| 中使用的類別        | [**NTDS 服務**](c-ntdsservice.md)<br/> |



 

 





