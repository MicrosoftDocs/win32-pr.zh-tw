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
ms.openlocfilehash: 437055ee9e1d33d4b551faf1ca999d432a99d17919dcd67f6a701bc4f9780543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428918"
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

 

 




