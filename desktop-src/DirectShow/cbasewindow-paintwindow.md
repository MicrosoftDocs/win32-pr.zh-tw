---
description: PaintWindow 方法會讓視窗重新繪製。
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: 'CBaseWindow. PaintWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cc998f270947890327fb3cbacce4a29183604047824b05b8a66538c163bdc08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635118"
---
# <a name="cbasewindowpaintwindow-method"></a>CBaseWindow. PaintWindow 方法

`PaintWindow`方法會讓視窗重新繪製。

## <a name="syntax"></a>語法


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bErase* 
</dt> <dd>

指定是否清除背景的布林值。 如果值為 **TRUE**，則會清除背景。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會藉 \_ 由使視窗的整個工作區失效，以產生 WM 繪製訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




