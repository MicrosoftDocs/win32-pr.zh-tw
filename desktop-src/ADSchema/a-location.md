---
title: Location 屬性
description: 使用者的位置，例如 office 號碼。
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- Location 屬性 AD 架構
- location 屬性 AD 架構
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a37f15e80d470c0662036745f285aea87e79391
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107892"
---
# <a name="location-attribute-ad-schema"></a>Location 屬性 (AD Schema) 

使用者的位置，例如 office 號碼。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | Location                                    |
| Ldap-顯示名稱 | location                                    |
| 大小              | \-                                          |
| 更新許可權  | \-                                          |
| 更新頻率  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| 系統識別碼-Guid    | 09dcb79f-165f-11d0-a064-00aa006c33ed        |
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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                               |
| System-Only            | 否                                                                                                                                                            |
| 是-單一值       | 對                                                                                                                                                             |
| 已編制索引             | 對                                                                                                                                                             |
| 在通用類別目錄中      | 對                                                                                                                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**網站**](c-site.md)<br/> [**子**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | 否                                                                                                                                                                                              |
| 是-單一值       | 對                                                                                                                                                                                               |
| 已編制索引             | 對                                                                                                                                                                                               |
| 在通用類別目錄中      | 對                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**房間**](c-room.md)<br/> [**網站**](c-site.md)<br/> [**子**](c-subnet.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | 否                                                                   |
| 是-單一值       | 對                                                                    |
| 已編制索引             | 對                                                                    |
| 在通用類別目錄中      | 對                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                            |
| Range-Lower            | 0                                                                       |
| Range-Upper            | 1024                                                                    |
| Search-Flags           | 0x00000001                                                              |
| System-Flags           | 0x00000010                                                              |
| 中使用的類別        | [**網站**](c-site.md)<br/> [**子**](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | 否                                                                                                                                                                                              |
| 是-單一值       | 對                                                                                                                                                                                               |
| 已編制索引             | 對                                                                                                                                                                                               |
| 在通用類別目錄中      | 對                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**房間**](c-room.md)<br/> [**網站**](c-site.md)<br/> [**子**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | 否                                                                                                                                                                                              |
| 是-單一值       | 對                                                                                                                                                                                               |
| 已編制索引             | 對                                                                                                                                                                                               |
| 在通用類別目錄中      | 對                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**房間**](c-room.md)<br/> [**網站**](c-site.md)<br/> [**子**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | 否                                                                                                                                                                                              |
| 是-單一值       | 對                                                                                                                                                                                               |
| 已編制索引             | 對                                                                                                                                                                                               |
| 在通用類別目錄中      | 對                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**房間**](c-room.md)<br/> [**網站**](c-site.md)<br/> [**子**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | 否                                                                                                                                                                                              |
| 是-單一值       | 對                                                                                                                                                                                               |
| 已編制索引             | 對                                                                                                                                                                                               |
| 在通用類別目錄中      | 對                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| 中使用的類別        | [**電腦**](c-computer.md)<br/> [**列印佇列**](c-printqueue.md)<br/> [**房間**](c-room.md)<br/> [**網站**](c-site.md)<br/> [**子**](c-subnet.md)<br/> |



 

 





