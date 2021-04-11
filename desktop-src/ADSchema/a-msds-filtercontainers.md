---
title: ms DS-篩選-容器屬性
description: 多重值的字串，其中包含類別名稱，這些類別是用來決定在篩選時應該由 Active Directory 消費者和電腦嵌入式管理單元顯示的容器類型。
ms.assetid: 765ac0e1-59d2-44a9-a01e-9cdf7d040c93
ms.tgt_platform: multiple
keywords:
- ms DS-篩選-容器屬性 AD 架構
- FilterContainers 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Filter-Containers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8156b1baa2fe86ec0322a9161ce5231a7e23f32e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108140"
---
# <a name="ms-ds-filter-containers-attribute"></a>ms DS-篩選-容器屬性

多重值的字串，其中包含類別名稱，這些類別是用來決定在篩選時應該由 Active Directory 消費者和電腦嵌入式管理單元顯示的容器類型。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | ms-DS-篩選-容器                     |
| Ldap-顯示名稱 | FilterContainers                       |
| 大小              | \-                                          |
| 更新許可權  | 網域系統管理員                        |
| 更新頻率  | 當容器類型清單變更時。   |
| Attribute-Id      | 1.2.840.113556.1.4.1703                     |
| 系統識別碼-Guid    | fb00dcdf-ac37-483a-9c12-ac53a6603033        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------------------------|
| 連結識別碼                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | 否                                               |
| 是-單一值       | 否                                               |
| 已編制索引             | 否                                               |
| 在通用類別目錄中      | 否                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                        |
| Range-Lower            | 1                                                   |
| Range-Upper            | 64                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| 中使用的類別        | [**DS-UI-設定**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------|
| 連結識別碼                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | 否                                               |
| 是-單一值       | 否                                               |
| 已編制索引             | 否                                               |
| 在通用類別目錄中      | 否                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                        |
| Range-Lower            | 1                                                   |
| Range-Upper            | 64                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| 中使用的類別        | [**DS-UI-設定**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------------------------|
| 連結識別碼                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | 否                                               |
| 是-單一值       | 否                                               |
| 已編制索引             | 否                                               |
| 在通用類別目錄中      | 否                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                        |
| Range-Lower            | 1                                                   |
| Range-Upper            | 64                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| 中使用的類別        | [**DS-UI-設定**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------|
| 連結識別碼                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | 否                                               |
| 是-單一值       | 否                                               |
| 已編制索引             | 否                                               |
| 在通用類別目錄中      | 否                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                        |
| Range-Lower            | 1                                                   |
| Range-Upper            | 64                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| 中使用的類別        | [**DS-UI-設定**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------------------------|
| 連結識別碼                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | 否                                               |
| 是-單一值       | 否                                               |
| 已編制索引             | 否                                               |
| 在通用類別目錄中      | 否                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                        |
| Range-Lower            | 1                                                   |
| Range-Upper            | 64                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| 中使用的類別        | [**DS-UI-設定**](c-dsuisettings.md)<br/> |



 

 





