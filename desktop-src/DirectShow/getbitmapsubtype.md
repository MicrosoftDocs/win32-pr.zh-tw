---
description: GetBitmapSubtype 函數會傳回指定點陣圖的媒體子類型 GUID。
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: 'GetBitmapSubtype 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8903e4a404367327b677a239b8ab28e3cb47e5679203857154f453a5cc01e25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536678"
---
# <a name="getbitmapsubtype-function"></a>GetBitmapSubtype 函式

函數會傳回 `GetBitmapSubtype` 指定點陣圖的媒體子類型 **GUID** 。

## <a name="syntax"></a>語法


```C++
const GUID GetBitmapSubtype(
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

傳回媒體子類型 **GUID**。

## <a name="remarks"></a>備註

針對未壓縮的 RGB 類型，此函式會將 **biBitCount** 欄位對應到子類型。 針對壓縮的影片類型，此函式會使用 [**FOURCCMap**](fourccmap.md) 類別，將 **biCompression** 欄位對應至子類型。

如果函式的格式不符合子類型，則傳回值為 GUID \_ Null。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




