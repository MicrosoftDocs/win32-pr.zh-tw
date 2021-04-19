---
description: GetBitmapSize 函式會計算與裝置無關的點陣圖 (DIB) 所需的位元組數目。 此函數只會呼叫 DIBSIZE 宏。
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: 'GetBitmapSize 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995320"
---
# <a name="getbitmapsize-function"></a>GetBitmapSize 函式

函 `GetBitmapSize` 式會計算與裝置無關的點陣圖 (DIB) 所需的位元組數目。 此函數只會呼叫 [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) 宏。

## <a name="syntax"></a>語法


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pHeader* 
</dt> <dd>

[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回以位元組為單位的大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




