---
title: ms DS-允許委派至屬性
description: 這是服務帳戶 (電腦或使用者帳戶) 物件的屬性。
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- ms DS-允許委派至屬性 AD 架構
- AllowedToDelegateTo 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973920"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a>ms DS-允許委派至屬性

這是服務帳戶 (電腦或使用者帳戶) 物件的屬性。 它包含)  (Spn 的服務主體名稱清單。 這個屬性是用來設定服務，讓它可以取得可用於限制委派的服務票證。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | 允許對委派的 ms DS                |
| Ldap-顯示名稱 | AllowedToDelegateTo                    |
| 大小              | 0到64K                                    |
| 更新許可權  | \-                                          |
| 更新頻率  | 很少                                |
| Attribute-Id      | 1.2.840.113556.1.4.1787                     |
| 系統識別碼-Guid    | 800d94d7-b7a1-42a1-b14d-7cae1423d07f        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------|
| 連結識別碼                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | 否                                                              |
| 是-單一值       | 否                                                              |
| 已編制索引             | 否                                                              |
| 在通用類別目錄中      | 否                                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------|
| 連結識別碼                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | 否                                                              |
| 是-單一值       | 否                                                              |
| 已編制索引             | 否                                                              |
| 在通用類別目錄中      | 否                                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------|
| 連結識別碼                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | 否                                                              |
| 是-單一值       | 否                                                              |
| 已編制索引             | 否                                                              |
| 在通用類別目錄中      | 否                                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------|
| 連結識別碼                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | 否                                                              |
| 是-單一值       | 否                                                              |
| 已編制索引             | 否                                                              |
| 在通用類別目錄中      | 否                                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------|
| 連結識別碼                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | 否                                                              |
| 是-單一值       | 否                                                              |
| 已編制索引             | 否                                                              |
| 在通用類別目錄中      | 否                                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





