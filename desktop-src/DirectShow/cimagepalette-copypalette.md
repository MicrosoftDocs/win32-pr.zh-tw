---
description: CopyPalette 方法會將元件從任何 VIDEOINFO 結構複製到任何調色盤 VIDEOINFO 結構。
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: 'CImagePalette. CopyPalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c6f645d134ccf5fa786ff59cf0bc6cd37211af0cb2571bbc9955e5bb6367a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055448"
---
# <a name="cimagepalettecopypalette-method"></a>CImagePalette. CopyPalette 方法

`CopyPalette`方法會將 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構中的元件複製到任何調色盤 **VIDEOINFO** 結構。

## <a name="syntax"></a>語法


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Psrc* 
</dt> <dd>

來源媒體類型的指標。

</dd> <dt>

*pDest* 
</dt> <dd>

目的地媒體類型的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果已複製元件，則傳回 S OK。 \_如果來源或目的地媒體類型沒有調色板，則傳回 FALSE。

## <a name="remarks"></a>備註

*PDest* 媒體類型必須是調色盤格式，且色彩深度為8位或更少。 *.Psrc* 媒體類型可以是任何具有調色板的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)類型，包括具有調色板專案的 YUV 和真色彩格式。 方法會將 *.psrc* 中的調色板專案複製到新的調色板，並將新的調色板附加至 *pDest*。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImagePalette 類別**](cimagepalette.md)
</dt> </dl>

 

 




