---
description: SetControlWindowPin 方法會設定要與之同步處理的 pin。
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: 'CBaseControlWindow. SetControlWindowPin 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9ab7cbb5d199b0908c2eb51ffb5a70eda7eb1336bd66a1645daad61b3202d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056708"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>CBaseControlWindow. SetControlWindowPin 方法

`SetControlWindowPin`方法會設定要與之同步處理的 pin。

## <a name="syntax"></a>語法


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

用來同步處理介面之 pin 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

此成員函式會將 m \_ pPin 成員變數設定為等於 pPin 參數。 如同在函式中所述，只有在已成功連接篩選器時，才能呼叫介面。 物件會透過這個成員函式傳遞給它應該同步處理的 pin;在大部分的情況下，它會判斷 pin 是否在有介面方法的情況下連線，並會在失敗時傳回 VFW \_ E \_ 未 \_ 連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




