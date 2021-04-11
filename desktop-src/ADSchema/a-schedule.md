---
title: Schedule 屬性
description: 排程 BLOB，如 Windows NT 作業服務所定義。 供複寫使用。
ms.assetid: 5eb6409d-3fb5-4368-8b7f-ce19567b7260
ms.tgt_platform: multiple
keywords:
- 排程屬性 AD 架構
- 排程屬性 AD 架構
topic_type:
- apiref
api_name:
- Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abf53e86f77ecffc872d8b007e32b1f964ae244e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107550"
---
# <a name="schedule-attribute"></a>Schedule 屬性

排程 BLOB，如 Windows NT 作業服務所定義。 供複寫使用。



| 進入 | 值 |
|-------------------|-------------------------------------------------------|
| CN                | 排程                                              |
| Ldap-顯示名稱 | schedule                                              |
| 大小              | \-                                                    |
| 更新許可權  | \-                                                    |
| 更新頻率  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.211                                |
| 系統識別碼-Guid    | dd712224-10e4-11d0-a05f-00aa006c33ed                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | 否                                                                                                                                                                                                                                                                            |
| 是-單一值       | 對                                                                                                                                                                                                                                                                             |
| 已編制索引             | 否                                                                                                                                                                                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> [**NTDS-Site-設定**](c-ntdssitesettings.md)<br/> [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> [**NTFRS-訂閱者**](c-ntfrssubscriber.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | 否                                                                                                                                                                                                                                                                            |
| 是-單一值       | 對                                                                                                                                                                                                                                                                             |
| 已編制索引             | 否                                                                                                                                                                                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> [**NTDS-Site-設定**](c-ntdssitesettings.md)<br/> [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> [**NTFRS-訂閱者**](c-ntfrssubscriber.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                                            |
| System-Only            | 否                                                                                                                                                         |
| 是-單一值       | 對                                                                                                                                                          |
| 已編制索引             | 否                                                                                                                                                         |
| 在通用類別目錄中      | 否                                                                                                                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                                    |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> [**NTDS-Site-設定**](c-ntdssitesettings.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | 否                                                                                                                                                                                                                                                                            |
| 是-單一值       | 對                                                                                                                                                                                                                                                                             |
| 已編制索引             | 否                                                                                                                                                                                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> [**NTDS-Site-設定**](c-ntdssitesettings.md)<br/> [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> [**NTFRS-訂閱者**](c-ntfrssubscriber.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | 否                                                                                                                                                                                                                                                                            |
| 是-單一值       | 對                                                                                                                                                                                                                                                                             |
| 已編制索引             | 否                                                                                                                                                                                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> [**NTDS-Site-設定**](c-ntdssitesettings.md)<br/> [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> [**NTFRS-訂閱者**](c-ntfrssubscriber.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | 否                                                                                                                                                                                                                                                                            |
| 是-單一值       | 對                                                                                                                                                                                                                                                                             |
| 已編制索引             | 否                                                                                                                                                                                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> [**NTDS-Site-設定**](c-ntdssitesettings.md)<br/> [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> [**NTFRS-訂閱者**](c-ntfrssubscriber.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | 否                                                                                                                                                                                                                                                                            |
| 是-單一值       | 對                                                                                                                                                                                                                                                                             |
| 已編制索引             | 否                                                                                                                                                                                                                                                                            |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| 中使用的類別        | [**NTDS 連接**](c-ntdsconnection.md)<br/> [**NTDS-Site-設定**](c-ntdssitesettings.md)<br/> [**NTFRS-複本集**](c-ntfrsreplicaset.md)<br/> [**NTFRS-訂閱者**](c-ntfrssubscriber.md)<br/> [**站台連結**](c-sitelink.md)<br/> |



 

 





