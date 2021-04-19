---
description: SlowRender 方法會使用 SetDIBitsToDevice 或 StretchDIBits 函數來繪製影片影像。
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: 'CDrawImage. SlowRender 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998611"
---
# <a name="cdrawimageslowrender-method"></a>CDrawImage. SlowRender 方法

`SlowRender`方法會使用 **SetDIBitsToDevice** 或 **StretchDIBits** 函式來繪製影片影像。

## <a name="syntax"></a>語法


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

包含影像之範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果 [**CDrawImage：： UsingImageAllocator**](cdrawimage-usingimageallocator.md) 傳回 **FALSE**，則 [**CDrawImage：:D rawimage**](cdrawimage-drawimage.md) 方法會使用 `SlowRender` 來繪製影片影像。 否則，DrawImage 會使用 **FastRender** 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::FastRender**](cdrawimage-fastrender.md)
</dt> </dl>

 

 




