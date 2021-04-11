---
title: ms-DS-其他 Dns-主機名稱屬性
description: 屬性是用來儲存電腦物件的其他 DNS 主機名稱。 當 DC 重新命名時，就會使用這個屬性。
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- ms DS-其他 Dns-主機名稱屬性 AD 架構
- AdditionalDnsHostName 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935431"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a>ms-DS-其他 Dns-主機名稱屬性

屬性是用來儲存電腦物件的其他 DNS 主機名稱。 這個屬性是在電腦重新命名時使用，或以 "netdom computername" 管理名稱。



| 進入 | 值 |
|-------------------|-----------------------------------------------------------------------------|
| CN                | ms-DS-其他 Dns-主機名稱                                              |
| Ldap-顯示名稱 | AdditionalDnsHostName                                                  |
| 大小              | 每個值都可以是2048個字元。 值的數目是大約1200值的資料庫限制。 |
| 更新許可權  | 此值是由系統所設定。                                            |
| 更新頻率  | 重新命名電腦時。                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1717                                                     |
| 系統識別碼-Guid    | 80863791-dbe9-4eb8-837e-7f0ab55d9ac7                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------|
| 連結識別碼                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | 對                                      |
| 是-單一值       | 否                                     |
| 已編制索引             | 否                                     |
| 在通用類別目錄中      | 否                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------|
| 連結識別碼                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | 對                                      |
| 是-單一值       | 否                                     |
| 已編制索引             | 否                                     |
| 在通用類別目錄中      | 否                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------|
| 連結識別碼                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | 對                                      |
| 是-單一值       | 否                                     |
| 已編制索引             | 否                                     |
| 在通用類別目錄中      | 否                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------|
| 連結識別碼                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | 對                                      |
| 是-單一值       | 否                                     |
| 已編制索引             | 否                                     |
| 在通用類別目錄中      | 否                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------|
| 連結識別碼                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | 對                                      |
| 是-單一值       | 否                                     |
| 已編制索引             | 否                                     |
| 在通用類別目錄中      | 否                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> |



 

 





