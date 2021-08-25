---
title: ms DS-配額-受信任的屬性
description: 指派配額之安全性主體的 SID。
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- ms DS-配額-受信任的屬性 AD 架構
- QuotaTrustee 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b453a3f48da5af7564fdb79f81d22a15a5b72450a68f22112c59ebfb2a749ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803618"
---
# <a name="ms-ds-quota-trustee-attribute"></a>ms DS-配額-受信任的屬性

指派配額之安全性主體的 SID。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms DS-配額-信任者                  |
| Ldap-顯示名稱 | QuotaTrustee                    |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1844              |
| 系統識別碼-Guid    | 16378906-4ea5-49be-a8d1-bfd41dff4f65 |
| Syntax            | [**(Sid) 的字串**](s-string-sid.md)  |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 是                                                          |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**ms-DS-配額-控制**](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 是                                                          |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**ms-DS-配額-控制**](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 是                                                          |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**ms-DS-配額-控制**](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 是                                                          |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**ms-DS-配額-控制**](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 是                                                          |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**ms-DS-配額-控制**](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 是                                                          |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**ms-DS-配額-控制**](c-msds-quotacontrol.md)<br/> |



 

 





