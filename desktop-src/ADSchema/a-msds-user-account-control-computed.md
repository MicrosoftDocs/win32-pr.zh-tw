---
title: ms DS-使用者-帳戶-控制項計算的屬性
description: 使用者帳戶-控制項計算很像 userAccountControl，但是屬性的值可能包含不會保存的額外位。
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- ms DS-使用者-帳戶-控制項計算的屬性 AD 架構
- 使用者帳戶-控制項計算的屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8747bddccdfa65222072592b7f418fd35529d987f9903d71cddf5e01556fec53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763258"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>ms DS-使用者-帳戶-控制項計算的屬性

**使用者帳戶-控制項計算** 很像 [**userAccountControl**](a-useraccountcontrol.md)，但是屬性的值可能包含不會保存的額外位。 計算的位包括下列各項。



| 值                | Iads 中定義的名稱 ()                      |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **UF \_ 鎖定**<br/>                   |
| 0x800000<br/>  | **UF \_ 密碼已 \_ 過期**<br/>         |
| 0x4000000<br/> | **UF \_ 部分 \_ 秘密 \_ 帳戶**<br/> |
| 0x8000000<br/> | **UF \_ 使用 \_ AES \_ 金鑰**<br/>            |



 

您可以在使用者 **帳戶控制** 參考頁面中 [**找到使用者帳戶控制項和使用者**](a-useraccountcontrol.md)帳戶控制 **計算** 的完整位清單， (對應到 [ [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset]) 或 [**使用者 \_ 資訊 \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008)結構的 [網路管理參考] 頁面。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms-DS-使用者-帳戶-控制項計算  |
| Ldap-顯示名稱 | 使用者-帳戶-控制項計算   |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| 系統識別碼-Guid    | 2cc4b836-b63f-4940-8d23-ea7acf06af56 |
| Syntax            | [**列舉型別**](s-enumeration.md) |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------|
| 連結識別碼                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | 否                                                             |
| 是-單一值       | 是                                                              |
| 已編制索引             | 否                                                             |
| 在通用類別目錄中      | 否                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
| 中使用的類別        | [**ms DS 可系結-物件**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



 

