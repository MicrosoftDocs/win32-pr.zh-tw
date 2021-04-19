---
description: GetTrueColorType 函式會取出影片子類型的人類可讀取名稱。
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: 'GetTrueColorType 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987125"
---
# <a name="gettruecolortype-function"></a>GetTrueColorType 函式

**GetTrueColorType** 函式會取出影片子類型的人類可讀取名稱。

## <a name="syntax"></a>語法


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pHeader* 
</dt> <dd>

[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的指標，此結構會定義點陣圖。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 MEDIASUBTYPE \_ RGB555 或 MEDIASUBTYPE \_ RGB565。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




