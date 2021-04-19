---
description: FastRender 方法會使用 BitBlt 或 StretchBlt 函數來繪製影片影像。
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: 'CDrawImage. FastRender 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981121"
---
# <a name="cdrawimagefastrender-method"></a>CDrawImage. FastRender 方法

`FastRender`方法會使用 **BitBlt** 或 **StretchBlt** 函式來繪製影片影像。

## <a name="syntax"></a>語法


```C++
void FastRender(
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

[**CDrawImage：:D rawimage**](cdrawimage-drawimage.md)方法會呼叫這個方法，但只有在連接的配置器是 [**CImageAllocator**](cimageallocator.md)物件時才會呼叫。 在此情況下，媒體範例保證是 [**CImageSample**](cimagesample.md) 物件。 **CImageSample** 物件使用 **CreateDIBSection** 函式來配置點陣圖的共用記憶體，讓您可以使用 **BitBlt** 或 **StretchBlt** 來繪製影像。

如果來源和目標矩形完全相符，這個方法會呼叫 **BitBlt** ，否則會呼叫 **StretchBlt** 。

如果篩選器不擁有配置器，則 **DrawImage** 方法會使用 [**CDrawImage：： SlowRender**](cdrawimage-slowrender.md) 來繪製影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




