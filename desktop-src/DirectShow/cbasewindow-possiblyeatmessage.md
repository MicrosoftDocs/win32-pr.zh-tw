---
description: PossiblyEatMessage 方法可讓衍生類別將訊息轉送到另一個視窗。
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: 'CBaseWindow. PossiblyEatMessage 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851f46d14f949a49c9422256f9b2bda1ba314e5789773121387e89c011f7a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016456"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>CBaseWindow. PossiblyEatMessage 方法

`PossiblyEatMessage`方法可讓衍生類別將訊息轉送到另一個視窗。

## <a name="syntax"></a>語法


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uMsg* 
</dt> <dd>

訊息識別碼。

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

如果轉寄訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。 基類會傳回 **FALSE**。

## <a name="remarks"></a>備註

在 [**CBaseWindow：： OnReceiveMessage**](cbasewindow-onreceivemessage.md) 方法處理訊息之前，它會呼叫 `PossiblyEatMessage` 。 如果 `PossiblyEatMessage` 傳回 **TRUE，則** **OnReceiveMessage** 會忽略該訊息。 衍生的類別可以覆寫， `PossiblyEatMessage` 以便將某些訊息轉送至擁有者視窗。 例如，衍生自 **CBaseWindow** 的 [**CBaseControlWindow**](cbasecontrolwindow.md)類別會轉送鍵盤和滑鼠訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




