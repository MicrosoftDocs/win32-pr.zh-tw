---
title: Member 屬性
description: 屬於群組的使用者清單。
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- 成員屬性 AD 架構
- 成員屬性 AD 架構
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106967384"
---
# <a name="member-attribute"></a>Member 屬性

屬於群組的使用者清單。



| 進入 | 值 |
|-------------------|-------------------------------------------------------|
| CN                | 成員                                                |
| Ldap-顯示名稱 | member                                                |
| 大小              | \-                                                    |
| 更新許可權  | 網域系統管理員                                  |
| 更新頻率  | 每次在群組中新增或移除使用者時。 |
| Attribute-Id      | 2.5.4.31                                              |
| 系統識別碼-Guid    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



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
|------------------------|-----------------------------------------------------------------------------------------|
| 連結識別碼                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | 否                                                                                   |
| 是-單一值       | 否                                                                                   |
| 已編制索引             | 否                                                                                   |
| 在通用類別目錄中      | 對                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| 中使用的類別        | [**Group**](c-group.md)<br/> [**名稱群組**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | 否                                                                                                                                 |
| 是-單一值       | 否                                                                                                                                 |
| 已編制索引             | 否                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| 中使用的類別        | [**Group**](c-group.md)<br/> [**名稱群組**](c-groupofnames.md)<br/> [**MSMQ 群組**](c-msmq-group.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|-------------------------------------|
| 連結識別碼                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | 否                               |
| 是-單一值       | 否                               |
| 已編制索引             | 否                               |
| 在通用類別目錄中      | 對                                |
| NT-Security-描述元 | O:BAG：不正確： S：                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| 中使用的類別        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | 否                                                                                                                                 |
| 是-單一值       | 否                                                                                                                                 |
| 已編制索引             | 否                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| 中使用的類別        | [**Group**](c-group.md)<br/> [**名稱群組**](c-groupofnames.md)<br/> [**MSMQ 群組**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | 否                                                                                                                                 |
| 是-單一值       | 否                                                                                                                                 |
| 已編制索引             | 否                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| 中使用的類別        | [**Group**](c-group.md)<br/> [**名稱群組**](c-groupofnames.md)<br/> [**MSMQ 群組**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | 否                                                                                                                                 |
| 是-單一值       | 否                                                                                                                                 |
| 已編制索引             | 否                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| 中使用的類別        | [**Group**](c-group.md)<br/> [**名稱群組**](c-groupofnames.md)<br/> [**MSMQ 群組**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | 否                                                                                                                                 |
| 是-單一值       | 否                                                                                                                                 |
| 已編制索引             | 否                                                                                                                                 |
| 在通用類別目錄中      | 對                                                                                                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| 中使用的類別        | [**Group**](c-group.md)<br/> [**名稱群組**](c-groupofnames.md)<br/> [**MSMQ 群組**](c-msmq-group.md)<br/> |



 

 





