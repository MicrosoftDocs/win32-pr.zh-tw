---
description: SetRealize 方法會指定視窗是否會發現調色板。
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: 'CBaseWindow. SetRealize 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991243"
---
# <a name="cbasewindowsetrealize-method"></a>CBaseWindow. SetRealize 方法

`SetRealize`方法會指定視窗是否會發現調色板。

## <a name="syntax"></a>語法


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bRealize* 
</dt> <dd>

指定是否要實現調色板的布林值。 若 **為 TRUE**， [**CBaseWindow：： SetPalette**](cbasewindow-setpalette.md) 方法會發現調色板。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

根據預設， **SetPalette** 方法會發現指定的調色板。 呼叫這個方法來變更預設行為，以選取但不能實現調色板。 這個方法會設定 [**CBaseWindow：： m \_ bNoRealize**](cbasewindow-m-bnorealize.md) 成員變數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




