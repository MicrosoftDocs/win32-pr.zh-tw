---
title: Manager 屬性
description: 包含使用者之管理員的分辨名稱。 管理員的使用者物件包含 directReports 屬性，其中包含所有使用者物件的參考，這些物件的管理員屬性都設為此辨別名稱。
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Manager 屬性 AD 架構
- manager 屬性 AD 架構
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385410"
---
# <a name="manager-attribute"></a>Manager 屬性

包含使用者之管理員的分辨名稱。 管理員的使用者物件包含 directReports 屬性，其中包含所有使用者物件的參考，這些物件的管理員屬性都設為此辨別名稱。



| 進入 | 值 |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| Ldap-顯示名稱 | manager                                                                     |
| 大小              | \-                                                                          |
| 更新許可權  | 網域系統管理員或帳戶擁有者。                                      |
| 更新頻率  | 當使用者的記錄建立時，以及每次管理員需要變更時。 |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| 系統識別碼-Guid    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------|
| 連結識別碼                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | 否                                                              |
| 是-單一值       | 對                                                               |
| 已編制索引             | 否                                                              |
| 在通用類別目錄中      | 對                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | 否                                                                                                                  |
| 是-單一值       | 對                                                                                                                   |
| 已編制索引             | 否                                                                                                                  |
| 在通用類別目錄中      | 對                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | 否                                                                                                                  |
| 是-單一值       | 對                                                                                                                   |
| 已編制索引             | 否                                                                                                                  |
| 在通用類別目錄中      | 對                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | 否                                                                                                                  |
| 是-單一值       | 對                                                                                                                   |
| 已編制索引             | 否                                                                                                                  |
| 在通用類別目錄中      | 對                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | 否                                                                                                                  |
| 是-單一值       | 對                                                                                                                   |
| 已編制索引             | 否                                                                                                                  |
| 在通用類別目錄中      | 對                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | 否                                                                                                                  |
| 是-單一值       | 對                                                                                                                   |
| 已編制索引             | 否                                                                                                                  |
| 在通用類別目錄中      | 對                                                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| 中使用的類別        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





