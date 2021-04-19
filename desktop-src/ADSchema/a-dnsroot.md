---
title: Dns-Root 屬性
description: 指派給網域/目錄分割的最上層 DNS 功能變數名稱。
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Dns-Root 屬性 AD 架構
- dnsRoot 屬性 AD 架構
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106968812"
---
# <a name="dns-root-attribute"></a>Dns-Root 屬性

指派給網域/目錄分割的最上層 DNS 功能變數名稱。 這是在交叉參考物件上設定的，並且用於參考產生的其他專案。 搜尋整個網域樹狀結構時，必須在 Dns-Root 物件起始搜尋。 這個屬性可以是多重值，在這種情況下，會產生多個參考。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| Ldap-顯示名稱 | dnsRoot                                     |
| 大小              | \-                                          |
| 更新許可權  | 此值是由系統所設定。            |
| 更新頻率  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| 系統識別碼-Guid    | bf967959-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|--------------------------------------------|
| 連結識別碼                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | 否                                      |
| 是-單一值       | 否                                      |
| 已編制索引             | 對                                       |
| 在通用類別目錄中      | 否                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------|
| 連結識別碼                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | 否                                      |
| 是-單一值       | 否                                      |
| 已編制索引             | 對                                       |
| 在通用類別目錄中      | 否                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|--------------------------------------------|
| 連結識別碼                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | 否                                      |
| 是-單一值       | 否                                      |
| 已編制索引             | 對                                       |
| 在通用類別目錄中      | 否                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------|
| 連結識別碼                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | 否                                      |
| 是-單一值       | 否                                      |
| 已編制索引             | 對                                       |
| 在通用類別目錄中      | 否                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------|
| 連結識別碼                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | 否                                      |
| 是-單一值       | 否                                      |
| 已編制索引             | 對                                       |
| 在通用類別目錄中      | 否                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------|
| 連結識別碼                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | 否                                      |
| 是-單一值       | 否                                      |
| 已編制索引             | 對                                       |
| 在通用類別目錄中      | 否                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------|
| 連結識別碼                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | 否                                      |
| 是-單一值       | 否                                      |
| 已編制索引             | 對                                       |
| 在通用類別目錄中      | 否                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> |



 

 





