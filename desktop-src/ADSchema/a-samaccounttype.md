---
title: SAM-Account-Type 屬性
description: 此屬性包含每個帳戶類型物件的相關資訊。
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- SAM-帳戶-類型屬性 AD 架構
- sAMAccountType 屬性 AD 架構
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935352"
---
# <a name="sam-account-type-attribute"></a>SAM-Account-Type 屬性

此屬性包含每個帳戶類型物件的相關資訊。 您可以列舉帳戶類型清單，也可以使用顯示資訊 API 來建立清單。 因為電腦、一般使用者帳戶和信任帳戶也可以列舉為使用者物件，所以這些帳戶的值必須是連續的範圍。

這個屬性的可能值如下：

-   SAM \_ 網域 \_ 物件0x0
-   SAM \_ 群組 \_ 物件0x10000000
-   SAM \_ 非 \_ 安全 \_ 組 \_ 物件0x10000001
-   SAM \_ 別名 \_ 物件0x20000000
-   SAM \_ 非 \_ 安全性 \_ 別名 \_ 物件0x20000001
-   SAM \_ 使用者 \_ 物件0x30000000
-   SAM \_ 一般 \_ 使用者 \_ 帳戶0x30000000
-   SAM \_ 電腦 \_ 帳戶0x30000001
-   SAM \_ 信任 \_ 帳戶0x30000002
-   SAM \_ 應用程式 \_ 基本 \_ 群組0x40000000
-   SAM \_ 應用程式 \_ 查詢 \_ 群組0x40000001
-   SAM \_ 帳戶 \_ 類型 \_ 最大的0x7fffffff



| 進入 | 值 |
|-------------------|-----------------------------------------------------------------|
| CN                | SAM-帳戶-類型                                                |
| Ldap-顯示名稱 | sAMAccountType                                                  |
| 大小              | \-                                                              |
| 更新許可權  | 此值是由系統所設定。                                |
| 更新頻率  | 這是在建立物件時由作業系統設定。 |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| 系統識別碼-Guid    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
| Syntax            | [**列舉型別**](s-enumeration.md)                            |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 對                                                         |
| 已編制索引             | 對                                                         |
| 在通用類別目錄中      | 對                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 對                                                         |
| 已編制索引             | 對                                                         |
| 在通用類別目錄中      | 對                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 對                                                         |
| 已編制索引             | 對                                                         |
| 在通用類別目錄中      | 對                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 對                                                         |
| 已編制索引             | 對                                                         |
| 在通用類別目錄中      | 對                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 對                                                         |
| 已編制索引             | 對                                                         |
| 在通用類別目錄中      | 對                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|--------------------------------------------------------------|
| 連結識別碼                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | 否                                                        |
| 是-單一值       | 對                                                         |
| 已編制索引             | 對                                                         |
| 在通用類別目錄中      | 對                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> |



 

 





