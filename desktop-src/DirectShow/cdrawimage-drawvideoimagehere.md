---
description: DrawVideoImageHere 方法會從媒體範例將影像繪製到指定的裝置內容。
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: 'CDrawImage. DrawVideoImageHere 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8137c4e18708ce6a0402d1d34caf9560054f267d8de0280a6efb5c3dd36e6517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909808"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>CDrawImage. DrawVideoImageHere 方法

`DrawVideoImageHere`方法會從媒體範例將影像繪製到指定的裝置內容。

## <a name="syntax"></a>語法


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hdc* 
</dt> <dd>

裝置內容的控制碼，將會在其中進行繪製。

</dd> <dt>

*pMediaSample* 
</dt> <dd>

包含影像之範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。

</dd> <dt>

*lprcSrc* 
</dt> <dd>

要用於繪圖的來源矩形指標。 如果是 **Null**，則會使用 [**CDrawImage：： m \_ SourceRect**](cdrawimage-m-sourcerect.md) 中的矩形。

</dd> <dt>

*lprcDst* 
</dt> <dd>

要用於繪圖的目標矩形指標。 如果是 **Null**，則會使用 [**CDrawImage：： m \_ TargetRect**](cdrawimage-m-targetrect.md) 中的矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




