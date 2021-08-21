---
description: Put \_ MessageDrain 方法會設定視窗，以接收傳送至影片轉譯器的視窗訊息。
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: 'CBaseControlWindow.put_MessageDrain 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b58ac59d83023530ca6da51efc2f84ba42c4bef9ac0d3f25ad9a234a320291f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017256"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>CBaseControlWindow. put \_ MessageDrain 方法

`put_MessageDrain`方法會將視窗設定為接收傳送至影片轉譯器的視窗訊息。

## <a name="syntax"></a>語法


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*清空* 
</dt> <dd>

要張貼訊息的時間範圍。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

傳送至影片轉譯器篩選器的訊息可以張貼至另一個視窗。 此成員函式會註冊視窗以接收這些訊息。 不同于 [**CBaseControlWindow：:p ui \_ 擁有**](cbasecontrolwindow-put-owner.md) 者成員函式，此成員函式不會讓影片視窗成為另一個視窗的子系。 它特別適用于全螢幕的影片轉譯器，它不能是子視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




