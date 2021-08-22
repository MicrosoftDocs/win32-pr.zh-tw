---
title: ms DS-使用者-帳戶-自動鎖定屬性
description: 指出此屬性參考的帳戶是否已被鎖定。
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- ms DS-使用者-帳戶-自動鎖定的屬性 AD 架構
- UserAccountAutoLocked 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1360b9169d5355ef23caf47fa56a283dc4e5267fb603aa08bd0600f126c69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119300298"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>ms DS-使用者-帳戶-自動鎖定屬性

指出此屬性參考的帳戶是否已被鎖定。如果帳戶遭到鎖定，則為 True;否則為 False。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms DS-使用者-帳戶-自動鎖定       |
| Ldap-顯示名稱 | UserAccountAutoLocked          |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| 系統識別碼-Guid    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
| Syntax            | [**Boolean**](s-boolean.md)         |



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
| System-Flags           | 0x00000014                                                        |
| 中使用的類別        | [**ms DS 可系結-物件**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>備註

在 ADAM 中，這個屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [**ADS \_ UF \_ 鎖定**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)旗標。

 

