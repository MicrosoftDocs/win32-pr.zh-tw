---
description: ContainsPalette 函式會判斷指定的 VIDEOINFOHEADER 結構是否包含調色板。
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: 'ContainsPalette 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c9e5ab793dfaadb868cc09cfbe25e59c02dc338b470992b81ab1990581e5c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954167"
---
# <a name="containspalette-function"></a>ContainsPalette 函式

**ContainsPalette** 函式會判斷指定的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構是否包含調色板。

## <a name="syntax"></a>語法


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

[**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 bitdepth 為8或小於 (**bmiHeader. biBitCount**) ，或色彩索引的數目大於零 (**bmiHeader. biClrUsed**) ，則會傳回 **TRUE** 。 否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




