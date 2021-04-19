---
description: 如果原生影片大小和媒體類型格式之間有差異，則 ScaleSourceRect 方法會調整矩形。
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: 'CDrawImage. ScaleSourceRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977625"
---
# <a name="cdrawimagescalesourcerect-method"></a>CDrawImage. ScaleSourceRect 方法

`ScaleSourceRect`如果原生影片大小和媒體類型格式之間有差異，則此方法會調整矩形。

## <a name="syntax"></a>語法


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSource* 
</dt> <dd>

未縮放矩形的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回縮放的矩形。

## <a name="remarks"></a>備註

在 **CDrawImage** 類別中，此方法會在沒有任何變更的情況下傳回 *pSource* 。 如果篩選器會延伸傳入的影片影像，您可以覆寫這個方法。 例如，原生影片大小可能是 320 240，但輸入釘選上的媒體類型可能是 640 480。 在這種情況下，篩選準則必須以2的因數調整來源矩形。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




