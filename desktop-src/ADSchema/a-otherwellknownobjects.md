---
title: 其他知名物件屬性
description: 包含依 GUID 和辨別名稱的容器清單。 這可讓您只使用 GUID 和功能變數名稱來移動物件。 只要移動物件，系統就會自動更新分辨名稱。
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- 其他知名物件的屬性 AD 架構
- otherWellKnownObjects 屬性 AD 架構
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467328"
---
# <a name="other-well-known-objects-attribute"></a>其他知名物件屬性

包含依 GUID 和辨別名稱的容器清單。 這可讓您只使用 GUID 和功能變數名稱來移動物件。 只要移動物件，系統就會自動更新分辨名稱。



| 進入 | 值 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | 其他知名物件                                                                                                                                                                                      |
| Ldap-顯示名稱 | otherWellKnownObjects                                                                                                                                                                                         |
| 大小              | 用來在 microsoft 網域中取出使用者容器的範例： LDAP:// (WKGUID = a9d1ca15768811d1aded00c04fd8d5cd，dc = microsoft，dc = com) 。 注意：以括弧取代角括弧，以避免 XML 衝突。 |
| 更新許可權  | 架構系統管理員                                                                                                                                                                                          |
| 更新頻率  | 每次移動物件時。                                                                                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1359                                                                                                                                                                                       |
| 系統識別碼-Guid    | 1ea64e5d-ac0f-11d2-90df-00c04fd91ab1                                                                                                                                                                          |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                               |



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
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



 

 





