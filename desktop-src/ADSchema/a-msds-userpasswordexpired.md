---
title: ms DS-使用者密碼-已過期屬性
description: 指出此屬性參考之帳戶的密碼是否已過期。
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- ms DS-使用者-密碼-過期屬性 AD 架構
- UserPasswordExpired 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d99143c470e58d1b1cb5e0cbd7e5302618ff0a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104187356"
---
# <a name="ms-ds-user-password-expired-attribute"></a>ms DS-使用者密碼-已過期屬性

指出此屬性參考之帳戶的密碼是否已過期。 如果密碼已過期，則為 True;否則為 False。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms-DS-使用者密碼-已過期          |
| Ldap-顯示名稱 | UserPasswordExpired             |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| 系統識別碼-Guid    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>實作

-   [**亞當**](#adam)

## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------|
| 連結識別碼                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | 否                                                             |
| 是-單一值       | 對                                                              |
| 已編制索引             | 否                                                             |
| 在通用類別目錄中      | 否                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
| 中使用的類別        | [**ms DS 可系結-物件**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>備註

在 ADAM 中，這個屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [ [**ADS 的 \_ UF 密碼已 \_ \_ 過期**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)] 旗標。

 

