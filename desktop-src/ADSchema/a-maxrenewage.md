---
title: 最大值-續約-存留期屬性
description: 這個屬性會決定使用者的票證授權票證 (TGT) 可針對 Kerberos 驗證進行更新的時間週期（以天為單位）。 預設值是預設網域中的7天群組原則物件 (GPO) 。
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- 最大-更新-存留期屬性 AD 架構
- maxRenewAge 屬性 AD 架構
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0068beff1f7d7af1ab66f01f7236dcc4b0116c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106966557"
---
# <a name="max-renew-age-attribute"></a>最大值-續約-存留期屬性

這個屬性會決定使用者的票證授權票證 (TGT) 可針對 Kerberos 驗證進行更新的時間週期（以天為單位）。 預設值是預設網域中的7天群組原則物件 (GPO) 。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | 最大續約-期限                        |
| Ldap-顯示名稱 | maxRenewAge                          |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.75                |
| 系統識別碼-Guid    | bf9679bc-0de6-11d0-a285-00aa003049e2 |
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
| 是-單一值       | 對                                               |
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
| 是-單一值       | 對                                               |
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
| 是-單一值       | 對                                               |
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
| 是-單一值       | 對                                               |
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
| 是-單一值       | 對                                               |
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
| 是-單一值       | 對                                               |
| 已編制索引             | 否                                              |
| 在通用類別目錄中      | 否                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> |



 

 





