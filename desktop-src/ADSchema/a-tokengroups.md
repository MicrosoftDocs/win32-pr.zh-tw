---
title: Token-Groups 屬性
description: 包含 Sid 清單的計算屬性，此屬性是由指定使用者或電腦上的可轉移群組成員資格擴充作業所造成。 如果沒有任何通用類別目錄可取得可轉移的反向成員資格，則無法抓取權杖群組。
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Token-Groups 屬性 AD 架構
- tokenGroups 屬性 AD 架構
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8971f9ba5baead73b7704760dcc86430f5ce1a318ac6bcbd9dfaf4125a21af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022066"
---
# <a name="token-groups-attribute"></a>Token-Groups 屬性

包含 Sid 清單的計算屬性，此屬性是由指定使用者或電腦上的可轉移群組成員資格擴充作業所造成。 如果沒有任何通用類別目錄可取得可轉移的反向成員資格，則無法抓取權杖群組。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | Token-Groups                         |
| Ldap-顯示名稱 | tokenGroups                          |
| 大小              | \-                                   |
| 更新許可權  | 此值是由系統所設定。     |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1301              |
| 系統識別碼-Guid    | b7c69e6d-2cc7-11d2-854e-00a0c983f608 |
| Syntax            | [**(Sid) 的字串**](s-string-sid.md)  |



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
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 否                                                        |
| 在通用類別目錄中      | 否                                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 否                                                        |
| 在通用類別目錄中      | 否                                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 否                                                        |
| 在通用類別目錄中      | 否                                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 否                                                        |
| 在通用類別目錄中      | 否                                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 否                                                        |
| 在通用類別目錄中      | 否                                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 否                                                        |
| 在通用類別目錄中      | 否                                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 否                                                        |
| 已編制索引             | 否                                                        |
| 在通用類別目錄中      | 否                                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



 

 





