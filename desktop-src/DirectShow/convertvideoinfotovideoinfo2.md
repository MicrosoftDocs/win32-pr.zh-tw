---
description: ConvertVideoInfoToVideoInfo2 函式會將使用 VIDEOINFOHEADER 的媒體類型轉換成一個使用 VIDEOINFOHEADER2 的媒體類型。
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: 'ConvertVideoInfoToVideoInfo2 函式 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f1865652edf01a612ba7d1a46520f92a8461c9ba53a80395e27e6252e0018ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073762"
---
# <a name="convertvideoinfotovideoinfo2-function"></a>ConvertVideoInfoToVideoInfo2 函式

`ConvertVideoInfoToVideoInfo2`函數會將使用 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)的媒體類型轉換成使用 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

要轉換的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。 結構的格式類型必須是 \_ VideoInfo。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 \_ [確定] 或 [E \_ OUTOFMEMORY]。

## <a name="remarks"></a>備註

此函式會配置新的 **VIDEOINFOHEADER2** 結構、將 **VIDEOINFOHEADER** 結構的成員複製到其中，然後以媒體類型的格式區塊中的新結構取代舊的結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片和影像函式](video-and-image-functions.md)
</dt> </dl>

 

 




