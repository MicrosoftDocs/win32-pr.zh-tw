---
title: User-Parameters 屬性
description: 使用者的參數。
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- User-Parameters 屬性 AD 架構
- userParameters 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f26907015ee1c17bc4e809b3b5c2a52adf79ffb20d497e34ff094b620936436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922928"
---
# <a name="user-parameters-attribute"></a>User-Parameters 屬性

使用者的參數。 指向保留給應用程式使用的 Unicode 字串。 這個字串可以是 null 字串，也可以在終止的 null 字元之前有任意數目的字元。 Microsoft 產品會使用這個成員來儲存個別程式專用的使用者資料。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | User-Parameters                             |
| Ldap-顯示名稱 | userParameters                              |
| 大小              | \-                                          |
| 更新許可權  | 由應用程式修改。                   |
| 更新頻率  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.138                      |
| 系統識別碼-Guid    | bf967a6d-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
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
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
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
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
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
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
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
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
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
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



 

 





