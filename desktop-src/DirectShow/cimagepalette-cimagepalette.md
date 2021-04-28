---
description: CImagePalette。 CImagePalette 函式-函數方法。
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: 'CImagePalette. CImagePalette (Winutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085676"
---
# <a name="cimagepalettecimagepalette-constructor"></a>CImagePalette. CImagePalette 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBaseFilter* 
</dt> <dd>

擁有篩選準則的指標。

</dd> <dt>

*pBaseWindow* 
</dt> <dd>

**CBaseWindow** 物件的指標，此物件會管理要實現調色板的視窗。 此參數可以是 **Null**。

</dd> <dt>

*pDrawImage* 
</dt> <dd>

**CDrawImage** 物件的指標，該物件會繪製影片影像。 此參數可以是 **Null**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImagePalette 類別**](cimagepalette.md)
</dt> </dl>

 

 




