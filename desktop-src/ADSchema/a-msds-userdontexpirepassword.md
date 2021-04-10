---
title: ms DS-使用者不過期-密碼屬性
description: 指出此屬性參考之帳戶的密碼是否會到期。
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- ms DS-使用者不過期-密碼屬性 AD 架構
- UserDontExpirePassword 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107766"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>ms DS-使用者不過期-密碼屬性

指出此屬性參考之帳戶的密碼是否會到期。 如果密碼不會過期，則為 True;否則為 False。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms DS-使用者不會過期-密碼      |
| Ldap-顯示名稱 | UserDontExpirePassword          |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| 系統識別碼-Guid    | 8788193a-2925-43d9-a221-bb7fff397675 |
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
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms DS 可系結-物件**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>備註

在 ADAM 中，此屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [ [**UF 未過期] \_ \_ \_ \_ 密碼**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)旗標。

 

