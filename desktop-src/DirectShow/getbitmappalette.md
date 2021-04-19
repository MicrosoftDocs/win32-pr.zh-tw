---
description: GetBitmapPalette 函數會傳回 VIDEOINFOHEADER 結構中的第一個調色板專案。
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: 'GetBitmapPalette 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999233"
---
# <a name="getbitmappalette-function"></a>GetBitmapPalette 函式

函數會傳回 `GetBitmapPalette` [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構中的第一個調色板專案。

## <a name="syntax"></a>語法


```C++
const RGBQUAD* GetBitmapPalette(
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

傳回第一個調色板專案的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




