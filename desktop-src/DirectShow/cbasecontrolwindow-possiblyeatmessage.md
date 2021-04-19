---
description: PossiblyEatMessage 方法會將鍵盤和滑鼠訊息轉送至訊息清空視窗。
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: 'CBaseControlWindow. PossiblyEatMessage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990604"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>CBaseControlWindow. PossiblyEatMessage 方法

方法會將 `PossiblyEatMessage` 鍵盤和滑鼠訊息轉送至訊息清空視窗。

## <a name="syntax"></a>語法


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uMsg* 
</dt> <dd>

視窗訊息。

</dd> <dt>

*wParam* 
</dt> <dd>

第一個訊息參數。

</dd> <dt>

*lParam* 
</dt> <dd>

第二個訊息參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息已轉送至視窗，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

[訊息清空] 視窗是指定用來接收特定滑鼠和鍵盤訊息的視窗。 視窗一開始是 **Null**;您可以藉由呼叫 [**CBaseControlWindow：:p 的 \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)來設定它。

如果訊息清空視窗為非 **Null**，則會將 `PossiblyEatMessage` 下列訊息張貼至該視窗：

-   WM \_ 字元
-   WM \_ DEADCHAR
-   WM \_ KEYDOWN
-   WM \_ KEYUP
-   WM \_ LBUTTONDBLCLK
-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDBLCLK
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEACTI加值稅E
-   WM \_ MOUSEMOVE
-   WM \_ NCLBUTTONDBLCLK
-   WM \_ NCLBUTTONDOWN
-   WM \_ NCLBUTTONUP
-   WM \_ NCMBUTTONDBLCLK
-   WM \_ NCMBUTTONDOWN
-   WM \_ NCMBUTTONUP
-   WM \_ NCMOUSEMOVE
-   WM \_ NCRBUTTONDBLCLK
-   WM \_ NCRBUTTONDOWN
-   WM \_ NCRBUTTONUP
-   WM \_ RBUTTONDBLCLK
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP
-   WM \_ SYSCHAR
-   WM \_ SYSDEADCHAR
-   WM \_ SYSKEYDOWN
-   WM \_ SYSKEYUP

它會忽略其他訊息。 如果訊息清空視窗為 **Null**，則方法會忽略所有視窗訊息。 如果它張貼訊息，方法會傳回 **TRUE** ，否則會傳回 **FALSE** 。 **CBaseWindow** 類別會在收到視窗訊息時呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




