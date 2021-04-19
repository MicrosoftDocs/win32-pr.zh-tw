---
title: AttemptLogin 方法
description: AttemptLogin 方法會顯示對話方塊，讓使用者可以嘗試登入線上商店。
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- attemptLogin 方法 Windows Media Player
- attemptLogin 方法 Windows Media Player、External 類別
- External class Windows Media Player，attemptLogin 方法
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976084"
---
# <a name="externalattemptlogin-method"></a>AttemptLogin 方法

**AttemptLogin** 方法會顯示對話方塊，讓使用者可以嘗試登入線上商店。

## <a name="syntax"></a>語法


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果登入嘗試導致登入狀態的變更，Windows Media Player 會引發 [OnLoginChange](external-onloginchange-event.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**OnLoginChange 事件**](external-onloginchange-event.md)
</dt> <dt>

[**UserLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner：： Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**管理登入**](managing-login.md)
</dt> </dl>

 

 





