---
title: ms-DS-使用者-密碼-非必要屬性
description: 指出這個屬性所參考的帳戶是否需要密碼。
ms.assetid: 86779c6f-d05c-409a-afe4-99ebf7c0593e
ms.tgt_platform: multiple
keywords:
- ms DS-使用者-密碼-不需要的屬性 AD 架構
- UserPasswordNotRequired 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Not-Required
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8ebb439af9a960d2dc0721940d9f4d2ab852b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108212"
---
# <a name="ms-ds-user-password-not-required-attribute"></a>ms-DS-使用者-密碼-非必要屬性

指出這個屬性所參考的帳戶是否需要密碼。 如果不需要密碼，則為 True;否則為 False。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms-DS-使用者-密碼-非必要     |
| Ldap-顯示名稱 | UserPasswordNotRequired        |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1854              |
| 系統識別碼-Guid    | 8f066172-a25e-4f53-8dcd-0a67d5fb883d |
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

在 ADAM 中，這個屬性會取代 [**userAccountControl**](a-useraccountcontrol.md)屬性的 [**ADS \_ UF \_ PASSWD \_ NOTREQD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum)旗標。

 

