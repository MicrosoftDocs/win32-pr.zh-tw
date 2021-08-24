---
title: User-Workstations 屬性
description: 包含執行 Windows NT 工作站或 Windows 2000 Professional 的電腦之 NetBIOS 或 DNS 名稱，使用者可從中登入。
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- User-Workstations 屬性 AD 架構
- userWorkstations 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe243275271088ed5634aa4a18ab053ecbad23ba6e844f8bbc18c5809cdfd72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702888"
---
# <a name="user-workstations-attribute"></a>User-Workstations 屬性

包含執行 Windows NT 工作站或 Windows 2000 Professional 的電腦之 NetBIOS 或 DNS 名稱，使用者可從中登入。 每個 NetBIOS 名稱會以逗號分隔。 多個名稱應以逗號分隔。

>[!Note]
>此使用者屬性不應再使用。 若要管理哪些帳戶可以登入哪些工作站，建議使用「允許本機登入」和「拒絕本機登入」或「允許登入遠端桌面服務」和「拒絕透過遠端桌面服務登入」。

| 進入 | 值 |
|-------------------|--------------------------------------------------------------------------------------------|
| CN                | User-Workstations                                                                          |
| Ldap-顯示名稱 | userWorkstations                                                                           |
| 大小              | \-                                                                                         |
| 更新許可權  | 網域系統管理員或帳戶擁有者。                                                     |
| 更新頻率  | 當使用者的記錄建立時，以及每次使用者的登入許可權需要變更時。 |
| Attribute-Id      | 1.2.840.113556.1.4.86                                                                      |
| 系統識別碼-Guid    | bf9679d7-0de6-11d0-a285-00aa003049e2                                                       |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



 

 





