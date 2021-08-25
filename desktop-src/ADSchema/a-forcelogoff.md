---
title: Force-Logoff 屬性
description: 用來計算 SamIGetAccountRestrictions 的啟動時間。 登出時間減去強制登出的時間等於啟動時間。
ms.assetid: 2ce1d5db-52aa-49c5-aef2-ec67122100ed
ms.tgt_platform: multiple
keywords:
- Force-Logoff 屬性 AD 架構
- forceLogoff 屬性 AD 架構
topic_type:
- apiref
api_name:
- Force-Logoff
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df1ab9721643edec3e03e91475c74e63dde94dcb982e0a84aad3cdf7c63b806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925848"
---
# <a name="force-logoff-attribute"></a>Force-Logoff 屬性

用來計算 SamIGetAccountRestrictions 的啟動時間。 登出時間減去強制登出的時間等於啟動時間。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | Force-Logoff                         |
| Ldap-顯示名稱 | forceLogoff                          |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.39                |
| 系統識別碼-Guid    | bf967977-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|----------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | 否                                                                                                    |
| 是-單一值       | 是                                                                                                     |
| 已編制索引             | 否                                                                                                    |
| 在通用類別目錄中      | 否                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | 否                                                                                                    |
| 是-單一值       | 是                                                                                                     |
| 已編制索引             | 否                                                                                                    |
| 在通用類別目錄中      | 否                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | 否                                                                                                    |
| 是-單一值       | 是                                                                                                     |
| 已編制索引             | 否                                                                                                    |
| 在通用類別目錄中      | 否                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | 否                                                                                                    |
| 是-單一值       | 是                                                                                                     |
| 已編制索引             | 否                                                                                                    |
| 在通用類別目錄中      | 否                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | 否                                                                                                    |
| 是-單一值       | 是                                                                                                     |
| 已編制索引             | 否                                                                                                    |
| 在通用類別目錄中      | 否                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | 否                                                                                                    |
| 是-單一值       | 是                                                                                                     |
| 已編制索引             | 否                                                                                                    |
| 在通用類別目錄中      | 否                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



 

 





