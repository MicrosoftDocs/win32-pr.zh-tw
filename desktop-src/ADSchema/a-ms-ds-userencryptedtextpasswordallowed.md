---
title: ms DS-使用者加密-文字-允許的屬性
description: 指出 Active Directory 是否會以可還原的加密格式儲存密碼。
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- ms DS-使用者加密-文字-允許的屬性 AD 架構
- UserEncryptedTextPasswordAllowed 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fc10b3facce4bef7cc5ff73abe9e901f67171dc2615b79c62355ac61a7c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118686999"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>ms DS-使用者加密-文字-允許的屬性

指出 Active Directory 是否會以可還原的加密格式儲存密碼。 如果密碼以可還原的加密格式儲存，則為 True;否則為 False。

> [!Note]  
> [Active Directory 輕量型目錄服務](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services)不會使用這個屬性，而且只會隨附于 userAccountControl 的完整性/同位。 AD LDS 不會以可還原的加密儲存密碼，無論此屬性在任何指定的物件上的值為何，或是與電腦本身的可還原加密有關的電腦安全性策略。

 



| 進入 | 值 |
|-------------------|--------------------------------------------|
| CN                | ms DS-使用者加密-文字-允許的密碼 |
| Ldap-顯示名稱 | UserEncryptedTextPasswordAllowed     |
| 大小              | \-                                         |
| 更新許可權  | \-                                         |
| 更新頻率  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| 系統識別碼-Guid    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Syntax            | [**Boolean**](s-boolean.md)               |



## <a name="implementations"></a>實作

-   [**亞當**](#adam)

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
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms DS 可系結-物件**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>備註

在 ADAM 中，這個屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [**ADS 已 \_ \_ 加密 \_ 文字 \_ 密碼 \_ 允許**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)旗標。

 

