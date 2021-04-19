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
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976538"
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

 

 




