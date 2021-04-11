---
title: Unicode-Pwd 屬性
description: Windows NT 單向格式的使用者密碼 (OWF) 。 Windows 2000 使用 Windows NT OWF。 這個屬性僅供作業系統使用。 請注意，您無法從密碼的 OWF 形式衍生出純文字密碼。
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Unicode-Pwd 屬性 AD 架構
- unicodePwd 屬性 AD 架構
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d00a1df180b7a30b56bdf198a78edc77cc99755
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107929"
---
# <a name="unicode-pwd-attribute"></a>Unicode-Pwd 屬性

Windows NT 單向格式的使用者密碼 (OWF) 。 Windows 2000 使用 Windows NT OWF。 這個屬性僅供作業系統使用。 請注意，您無法從密碼的 OWF 形式衍生出純文字密碼。



| 進入 | 值 |
|-------------------|------------------------------------------------------------------------------|
| CN                | Unicode-Pwd                                                                  |
| Ldap-顯示名稱 | unicodePwd                                                                   |
| 大小              | \-                                                                           |
| 更新許可權  | 網域系統管理員或帳戶擁有者。                                       |
| 更新頻率  | 當使用者的記錄建立時，以及每次需要變更密碼時。 |
| Attribute-Id      | 1.2.840.113556.1.4.90                                                        |
| 系統識別碼-Guid    | bf9679e1-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                        |



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
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------|
| 連結識別碼                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | 否                                                             |
| 是-單一值       | 對                                                              |
| 已編制索引             | 否                                                             |
| 在通用類別目錄中      | 否                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms DS 可系結-物件**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



 

 





