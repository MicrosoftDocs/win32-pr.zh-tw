---
title: SD-Rights-有效屬性
description: 此結構化屬性會傳回單一 DWORD 值，最多可以有三個位設定擁有者 \_ 安全性 \_ INFORMATIONDACL \_ 安全性 \_ INFORMATIONSACL \_ 安全性 \_ 資訊（如果已設定位），然後使用者就可以對安全描述項的對應部分進行寫入存取。 擁有者表示擁有者和群組。
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- SD-Rights-有效的屬性 AD 架構
- sDRightsEffective 屬性 AD 架構
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844935"
---
# <a name="sd-rights-effective-attribute"></a>SD-Rights-有效屬性

這個已建立的屬性會傳回單一 **DWORD** 值，最多可設定三個位：

-   擁有者 \_ 安全性 \_ 資訊
-   DACL \_ 安全性 \_ 資訊
-   SACL \_ 安全性 \_ 資訊

如果設定了位，則使用者會擁有安全描述項之對應部分的寫入權限。 擁有者表示擁有者和群組。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | SD-Rights-有效                  |
| Ldap-顯示名稱 | sDRightsEffective                    |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1304              |
| 系統識別碼-Guid    | c3dbafa6-33df-11d2-98b2-0000f87a57d4 |
| Syntax            | [**列舉型別**](s-enumeration.md) |



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
| 是-單一值       | 對                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 對                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 對                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 對                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 對                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 對                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 否                           |
| 是-單一值       | 對                            |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 否                           |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



 

 





