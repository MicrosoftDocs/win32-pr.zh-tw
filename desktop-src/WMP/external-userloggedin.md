---
title: UserLoggedIn
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |UserLoggedIn
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- UserLoggedIn Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976083"
---
# <a name="externaluserloggedin"></a>UserLoggedIn

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**UserLoggedIn** 屬性會抓取一個值，指出使用者是否已登入線上商店。

## <a name="syntax"></a>Syntax

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林值**。 **TRUE** 表示使用者已登入，而 **FALSE** 表示使用者已登出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**AttemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**OnLoginChange 事件**](external-onloginchange-event.md)
</dt> </dl>

 

 





