---
title: Search-Guide 屬性
description: 指定建議搜尋條件的資訊，這些資訊可能會包含在預期會是搜尋作業的方便基底物件的某些專案中，例如國家/地區或組織。
ms.assetid: 69823ef3-efa8-4732-bbec-27ed8fec81cc
ms.tgt_platform: multiple
keywords:
- Search-Guide 屬性 AD 架構
- searchGuide 屬性 AD 架構
topic_type:
- apiref
api_name:
- Search-Guide
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711202ebc39649e7e1aea2a4459c3a7147eb2ff6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973099"
---
# <a name="search-guide-attribute"></a>Search-Guide 屬性

指定建議搜尋條件的資訊，這些資訊可能會包含在預期會是搜尋作業的方便基底物件的某些專案中，例如國家/地區或組織。



| 進入 | 值 |
|-------------------|-------------------------------------------------------|
| CN                | Search-Guide                                          |
| Ldap-顯示名稱 | searchGuide                                           |
| 大小              | \-                                                    |
| 更新許可權  | 網域系統管理員                                  |
| 更新頻率  | 每次需要新的搜尋指南時。               |
| Attribute-Id      | 2.5.4.14                                              |
| 系統識別碼-Guid    | bf967a2e-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                                                                                                     |
| 是-單一值       | 否                                                                                                                                                                                                                                                                     |
| 已編制索引             | 否                                                                                                                                                                                                                                                                     |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**國家/地區**](c-country.md)<br/> [**位置**](c-locality.md)<br/> [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                                                                                                     |
| 是-單一值       | 否                                                                                                                                                                                                                                                                     |
| 已編制索引             | 否                                                                                                                                                                                                                                                                     |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**國家/地區**](c-country.md)<br/> [**位置**](c-locality.md)<br/> [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                 |
| MAPI-Id                | 0x812E                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                              |
| 在通用類別目錄中      | 否                                                                                                                                                                                              |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| 中使用的類別        | [**國家/地區**](c-country.md)<br/> [**位置**](c-locality.md)<br/> [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                                                                                                     |
| 是-單一值       | 否                                                                                                                                                                                                                                                                     |
| 已編制索引             | 否                                                                                                                                                                                                                                                                     |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**國家/地區**](c-country.md)<br/> [**位置**](c-locality.md)<br/> [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                                                                                                     |
| 是-單一值       | 否                                                                                                                                                                                                                                                                     |
| 已編制索引             | 否                                                                                                                                                                                                                                                                     |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**國家/地區**](c-country.md)<br/> [**位置**](c-locality.md)<br/> [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                                                                                                     |
| 是-單一值       | 否                                                                                                                                                                                                                                                                     |
| 已編制索引             | 否                                                                                                                                                                                                                                                                     |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**國家/地區**](c-country.md)<br/> [**位置**](c-locality.md)<br/> [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                                                                                                     |
| 是-單一值       | 否                                                                                                                                                                                                                                                                     |
| 已編制索引             | 否                                                                                                                                                                                                                                                                     |
| 在通用類別目錄中      | 否                                                                                                                                                                                                                                                                     |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**國家/地區**](c-country.md)<br/> [**位置**](c-locality.md)<br/> [**組織**](c-organization.md)<br/> [**組織單位**](c-organizationalunit.md)<br/> |



 

 





