---
title: ms DS-使用者-帳戶-已停用的屬性
description: 指出帳戶為停用或啟用。
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- ms DS-使用者-帳戶-停用的屬性 AD 架構
- Msds-useraccountdisabled 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f0744cd835fab641de4f4d3386304a342fe3902fcf1a67b3367dc15b7ee68f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544138"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>ms DS-使用者-帳戶-已停用的屬性

指出帳戶為停用或啟用。 如果帳戶已停用，則為 True;否則為 False。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms DS-使用者-帳戶-已停用          |
| Ldap-顯示名稱 | Msds-useraccountdisabled             |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| 系統識別碼-Guid    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
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
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms DS 可系結-物件**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>備註

在 ADAM 中，這個屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [**ADS \_ UF \_ ACCOUNTDISABLE**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)旗標。

 

