---
title: Instance-Type 屬性
description: 用來指定如何在特定伺服器上具現化物件的位位。
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Instance-Type 屬性 AD 架構
- instanceType 屬性 AD 架構
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb087afedfb6570c2d25858ca99a53749607f2260f3a6f7a24ae766e22ea3e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925278"
---
# <a name="instance-type-attribute"></a>Instance-Type 屬性

用來指定如何在特定伺服器上具現化物件的位位。 即使複本已同步，這個屬性的值也可能會在不同的複本上有所不同。

這個屬性可以是零或一或多個下列值的組合。

| 值      | 描述                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | 命名內容的標頭。                                                                        |
| 0x00000002 | 此複本未具現化。                                                                  |
| 0x00000004 | 此物件在此目錄中為可寫入。                                                          |
| 0x00000008 | 此目錄上的命名內容會保留在此目錄上。                                       |
| 0x00000010 | 命名內容正在使用複寫進行第一次的結構處理。 |
| 0x00000020 | 正在從本機 DSA 移除命名內容。                          |



 



| 進入 | 值 |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| Ldap-顯示名稱 | instanceType                                   |
| 大小              | 4個位元組。                                       |
| 更新許可權  | 此值是由架構管理員所設定。 |
| 更新頻率  | 建立物件時。                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| 系統識別碼-Guid    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Syntax            | [**列舉型別**](s-enumeration.md)           |



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
| MAPI-Id                | 0x80BD                          |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | 是                            |
| 是-單一值       | 是                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



 

 





