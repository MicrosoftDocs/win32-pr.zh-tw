---
title: UAS-Compat 屬性
description: 指出安全性帳戶管理員是否會強制執行資料大小，使 Active Directory 與 LanManager 使用者帳戶系統相容 (的) 。
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- UAS-Compat 屬性 AD 架構
- uASCompat 屬性 AD 架構
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970661"
---
# <a name="uas-compat-attribute"></a>UAS-Compat 屬性

指出安全性帳戶管理員是否會強制執行資料大小，使 Active Directory 與 LanManager 使用者帳戶系統相容 (的) 。 如果這個值為0，則不會強制執行任何限制。 如果這個值是1，則會強制執行下列限制。



| 值                          | 長度                         |
|--------------------------------|--------------------------------|
| 密碼<br/>            | 0到14個字元<br/>  |
| 帳戶名稱<br/>        | 0到20個字元<br/>  |
| 網域名稱<br/>         | 0到15個字元<br/>  |
| 電腦名稱<br/>       | 0到15個字元<br/>  |
| 註解<br/>            | 0到48個字元<br/>  |
| 主目錄<br/>      | 0到256個字元<br/> |
| 腳本路徑<br/>         | 0到256個字元<br/> |
| 每週的時間單位<br/> | 168個位 (21 個位元組) <br/> |



 



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| Ldap-顯示名稱 | uASCompat                            |
| 大小              | \-                                   |
| 更新許可權  | 由系統管理員執行。       |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| 系統識別碼-Guid    | bf967a61-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**列舉型別**](s-enumeration.md) |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|-------------------------------------------------------|
| 連結識別碼                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | 否                                                 |
| 是-單一值       | 對                                                  |
| 已編制索引             | 否                                                 |
| 在通用類別目錄中      | 否                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------|
| 連結識別碼                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | 否                                                 |
| 是-單一值       | 對                                                  |
| 已編制索引             | 否                                                 |
| 在通用類別目錄中      | 否                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------|
| 連結識別碼                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | 否                                                 |
| 是-單一值       | 對                                                  |
| 已編制索引             | 否                                                 |
| 在通用類別目錄中      | 否                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------|
| 連結識別碼                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | 否                                                 |
| 是-單一值       | 對                                                  |
| 已編制索引             | 否                                                 |
| 在通用類別目錄中      | 否                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------|
| 連結識別碼                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | 否                                                 |
| 是-單一值       | 對                                                  |
| 已編制索引             | 否                                                 |
| 在通用類別目錄中      | 否                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------|
| 連結識別碼                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | 否                                                 |
| 是-單一值       | 對                                                  |
| 已編制索引             | 否                                                 |
| 在通用類別目錄中      | 否                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



 

 





