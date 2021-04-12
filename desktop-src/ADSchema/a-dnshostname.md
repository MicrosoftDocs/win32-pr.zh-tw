---
title: DNS-主機名稱屬性
description: 在 DNS 中註冊的電腦名稱稱。
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- DNS-主機名稱屬性 AD 架構
- dNSHostName 屬性 AD 架構
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7580a58e5d3042633a9dd665354bc883b4fdb87c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509534"
---
# <a name="dns-host-name-attribute"></a>DNS-主機名稱屬性

在 DNS 中註冊的電腦名稱稱。



| 進入 | 值 |
|-------------------|-----------------------------------------------------------------------------|
| CN                | DNS-主機名稱                                                               |
| Ldap-顯示名稱 | dNSHostName                                                                 |
| 大小              | 每個區段可以是63個字元。 整個長度可以是255個字元。 |
| 更新許可權  | 網域系統管理員                                                        |
| 更新頻率  | 當電腦命名時。                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| 系統識別碼-Guid    | 72e39547-7b18-11d1-adef-00c04fd8d5cd                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | 否                                                                                                                                                                                                                      |
| 是-單一值       | 對                                                                                                                                                                                                                       |
| 已編制索引             | 否                                                                                                                                                                                                                      |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**電腦**](c-computer.md)<br/> [**PKI-註冊-服務**](c-pkienrollmentservice.md)<br/> [**伺服器**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | 否                                                                                                                                                                                                                      |
| 是-單一值       | 對                                                                                                                                                                                                                       |
| 已編制索引             | 否                                                                                                                                                                                                                      |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**電腦**](c-computer.md)<br/> [**PKI-註冊-服務**](c-pkienrollmentservice.md)<br/> [**伺服器**](c-server.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------------|
| 連結識別碼                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | 否                                 |
| 是-單一值       | 對                                  |
| 已編制索引             | 否                                 |
| 在通用類別目錄中      | 對                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                          |
| Range-Lower            | 0                                     |
| Range-Upper            | 2048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| 中使用的類別        | [**伺服器**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | 否                                                                                                                                                                                                                      |
| 是-單一值       | 對                                                                                                                                                                                                                       |
| 已編制索引             | 否                                                                                                                                                                                                                      |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**電腦**](c-computer.md)<br/> [**PKI-註冊-服務**](c-pkienrollmentservice.md)<br/> [**伺服器**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | 否                                                                                                                                                                                                                      |
| 是-單一值       | 對                                                                                                                                                                                                                       |
| 已編制索引             | 否                                                                                                                                                                                                                      |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**電腦**](c-computer.md)<br/> [**PKI-註冊-服務**](c-pkienrollmentservice.md)<br/> [**伺服器**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | 否                                                                                                                                                                                                                      |
| 是-單一值       | 對                                                                                                                                                                                                                       |
| 已編制索引             | 否                                                                                                                                                                                                                      |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**電腦**](c-computer.md)<br/> [**PKI-註冊-服務**](c-pkienrollmentservice.md)<br/> [**伺服器**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | 否                                                                                                                                                                                                                      |
| 是-單一值       | 對                                                                                                                                                                                                                       |
| 已編制索引             | 否                                                                                                                                                                                                                      |
| 在通用類別目錄中      | 對                                                                                                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| 中使用的類別        | [**憑證授權單位單位**](c-certificationauthority.md)<br/> [**電腦**](c-computer.md)<br/> [**PKI-註冊-服務**](c-pkienrollmentservice.md)<br/> [**伺服器**](c-server.md)<br/> |



 

 





