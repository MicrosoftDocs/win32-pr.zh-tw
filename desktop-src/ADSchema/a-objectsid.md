---
title: Object-Sid 屬性
description: 二進位值，指定使用者 (SID) 的安全識別碼。 SID 是用來將使用者識別為安全性主體的唯一值。
ms.assetid: 78ef0158-f59e-43df-b3fc-fb0f709936f6
ms.tgt_platform: multiple
keywords:
- Object-Sid 屬性 AD 架構
- objectSid 屬性 AD 架構
topic_type:
- apiref
api_name:
- Object-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf21d8806d904185c01e8831b8597c6cd69424f82789c1e419ec38e3be4dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442358"
---
# <a name="object-sid-attribute"></a>Object-Sid 屬性

二進位值，指定使用者 (SID) 的安全識別碼。 SID 是用來將使用者識別為安全性主體的唯一值。



| 進入 | 值 |
|-------------------|--------------------------------------------------------------|
| CN                | Object-Sid                                                   |
| Ldap-顯示名稱 | objectSid                                                    |
| 大小              | \-                                                           |
| 更新許可權  | 此值是由系統所設定。                             |
| 更新頻率  | 建立帳戶時，系統會設定此值。 |
| Attribute-Id      | 1.2.840.113556.1.4.146                                       |
| 系統識別碼-Guid    | bf9679e8-0de6-11d0-a285-00aa003049e2                         |
| Syntax            | [**(Sid) 的字串**](s-string-sid.md)                          |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | 否                                                                                                                                                                                                                                                      |
| 是-單一值       | 是                                                                                                                                                                                                                                                       |
| 已編制索引             | 是                                                                                                                                                                                                                                                       |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| 中使用的類別        | [**外部安全性-主體**](c-foreignsecurityprincipal.md)<br/> [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | 是                                                                                                                                                                                                                                                       |
| 是-單一值       | 是                                                                                                                                                                                                                                                       |
| 已編制索引             | 是                                                                                                                                                                                                                                                       |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| 中使用的類別        | [**外部安全性-主體**](c-foreignsecurityprincipal.md)<br/> [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                               |
| MAPI-Id                | 0x8027                                                                                                                                                                                           |
| System-Only            | 是                                                                                                                                                                                             |
| 是-單一值       | 是                                                                                                                                                                                             |
| 已編制索引             | 是                                                                                                                                                                                             |
| 在通用類別目錄中      | 是                                                                                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                |
| Range-Upper            | 28                                                                                                                                                                                               |
| Search-Flags           | 0x00000009                                                                                                                                                                                       |
| System-Flags           | 0x00000012                                                                                                                                                                                       |
| 中使用的類別        | [**外部安全性-主體**](c-foreignsecurityprincipal.md)<br/> [**ms DS-系結-Proxy**](c-msds-bindproxy.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | 是                                                                                                                                                                                                                                                       |
| 是-單一值       | 是                                                                                                                                                                                                                                                       |
| 已編制索引             | 是                                                                                                                                                                                                                                                       |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| 中使用的類別        | [**外部安全性-主體**](c-foreignsecurityprincipal.md)<br/> [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | 是                                                                                                                                                                                                                                                       |
| 是-單一值       | 是                                                                                                                                                                                                                                                       |
| 已編制索引             | 是                                                                                                                                                                                                                                                       |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| 中使用的類別        | [**外部安全性-主體**](c-foreignsecurityprincipal.md)<br/> [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | 是                                                                                                                                                                                                                                                       |
| 是-單一值       | 是                                                                                                                                                                                                                                                       |
| 已編制索引             | 是                                                                                                                                                                                                                                                       |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| 中使用的類別        | [**外部安全性-主體**](c-foreignsecurityprincipal.md)<br/> [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | 是                                                                                                                                                                                                                                                       |
| 是-單一值       | 是                                                                                                                                                                                                                                                       |
| 已編制索引             | 是                                                                                                                                                                                                                                                       |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| 中使用的類別        | [**外部安全性-主體**](c-foreignsecurityprincipal.md)<br/> [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> |



 

 





