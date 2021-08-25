---
title: 使用者主體名稱屬性
description: 此屬性包含 UPN，其為以網際網路標準 RFC 822 為基礎之使用者的網際網路樣式登入名稱。
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- 使用者主體名稱屬性 AD 架構
- userPrincipalName 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba8ac5196de660c4cff4b90801470581cc660491902ec5b48f0ced8337c498b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835283"
---
# <a name="user-principal-name-attribute"></a>使用者主體名稱屬性

此屬性包含 UPN，其為以網際網路標準 [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)為基礎之使用者的網際網路樣式登入名稱。 UPN 比分辨名稱短，而且更容易記住。 依照慣例，這應該對應到使用者的電子郵件名稱。 為此屬性設定的值等於使用者識別碼和功能變數名稱的長度。 如需此屬性的詳細資訊，請參閱 [使用者命名屬性](/windows/desktop/AD/naming-properties)。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | 使用者主體名稱                         |
| Ldap-顯示名稱 | userPrincipalName                           |
| 大小              | \-                                          |
| 更新許可權  | 網域系統管理員或帳戶擁有者。      |
| 更新頻率  | 理論上，這絕對不會改變。         |
| Attribute-Id      | 1.2.840.113556.1.4.656                      |
| 系統識別碼-Guid    | 28630ebb-41d5-11d1-a9c1-0000f80367c1        |
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
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 是                              |
| 在通用類別目錄中      | 是                              |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 是                              |
| 在通用類別目錄中      | 是                              |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|--------------|
| 連結識別碼                | \-           |
| MAPI-Id                | \-           |
| System-Only            | 否        |
| 是-單一值       | 是         |
| 已編制索引             | 是         |
| 在通用類別目錄中      | 是         |
| NT-Security-描述元 | O:BAG：不正確： S： |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000001   |
| System-Flags           | 0x00000012   |
| 中使用的類別        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 是                              |
| 在通用類別目錄中      | 是                              |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 是                              |
| 在通用類別目錄中      | 是                              |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 是                              |
| 在通用類別目錄中      | 是                              |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 是                              |
| 在通用類別目錄中      | 是                              |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="remarks"></a>備註

在 ADAM 中，此屬性不需要採用網際網路標準 RFC 822 格式;它可以是簡單名稱。

 

