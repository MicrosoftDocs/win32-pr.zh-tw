---
title: ms-TAPI-唯一識別碼屬性
description: 提供 TAPI 多播會議的名稱。 它是 Rt-Conference 類別的命名屬性。
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- ms-TAPI-唯一識別碼屬性 AD 架構
- msTAPI-uid 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385382"
---
# <a name="ms-tapi-unique-identifier-attribute"></a>ms-TAPI-唯一識別碼屬性

提供 TAPI 多播會議的名稱。 它是 Rt-Conference 類別的命名屬性。



| 進入 | 值 |
|-------------------|-----------------------------------------------------------------------|
| CN                | ms-TAPI-唯一識別碼                                             |
| Ldap-顯示名稱 | msTAPI-uid                                                            |
| 大小              | 可以是任一字元串，其長度通常低於100個字元。 |
| 更新許可權  | 不需要任何特殊許可權。                                       |
| 更新頻率  | 在建立 Rt-Conference 物件時設定一次。            |
| Attribute-Id      | 1.2.840.113556.1.4.1698                                               |
| 系統識別碼-Guid    | 70a4e7ea-b3b9-4643-8918-e6dd2471bfd4                                  |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                           |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | 否                                                                                                                       |
| 是-單一值       | 對                                                                                                                        |
| 已編制索引             | 否                                                                                                                       |
| 在通用類別目錄中      | 否                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> [**ms-TAPI-Rt-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | 否                                                                                                                       |
| 是-單一值       | 對                                                                                                                        |
| 已編制索引             | 否                                                                                                                       |
| 在通用類別目錄中      | 否                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> [**ms-TAPI-Rt-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | 否                                                                                                                       |
| 是-單一值       | 對                                                                                                                        |
| 已編制索引             | 否                                                                                                                       |
| 在通用類別目錄中      | 否                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> [**ms-TAPI-Rt-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | 否                                                                                                                       |
| 是-單一值       | 對                                                                                                                        |
| 已編制索引             | 否                                                                                                                       |
| 在通用類別目錄中      | 否                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> [**ms-TAPI-Rt-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | 否                                                                                                                       |
| 是-單一值       | 對                                                                                                                        |
| 已編制索引             | 否                                                                                                                       |
| 在通用類別目錄中      | 否                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> [**ms-TAPI-Rt-Person**](c-mstapi-rtperson.md)<br/> |



 

 





