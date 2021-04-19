---
description: DrawImage 方法會在影片視窗上繪製一個影片畫面。
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: 'CDrawImage. DrawImage 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976041"
---
# <a name="cdrawimagedrawimage-method"></a>CDrawImage. DrawImage 方法

`DrawImage`方法會在影片視窗上繪製一個影片畫面。

## <a name="syntax"></a>語法


```C++
BOOL DrawImage(
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

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會委派給 [**CDrawImage：： FastRender**](cdrawimage-fastrender.md) 或 [**CDrawImage：： SlowRender**](cdrawimage-slowrender.md)，這取決於篩選準則是否擁有提供範例的配置器。 如果篩選準則擁有配置器，則會保證範例是 [**CImageSample**](cimagesample.md) 物件。 在此情況下，此範例會使用 GDI 所配置的共用記憶體，而且可以使用 **BitBlt** 或 **StretchBlt** 來繪製影像。 否則，必須使用較慢的 **SetDIBitsToDevice** 或 **StretchDIBits** 函數來繪製影像。

在 debug 組建中，此方法會呼叫 **DisplaySampleTimes** ，以在影片影像上繪製範例的時間戳記。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




