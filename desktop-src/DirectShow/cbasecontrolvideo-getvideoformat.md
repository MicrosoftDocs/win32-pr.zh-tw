---
description: GetVideoFormat 方法會抓取表示目前影片格式的影片範例。
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: 'CBaseControlVideo. GetVideoFormat 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e37a59b8d002a9c081de74c4974dca1f86d1c9d0a5f7f7b0caca11be6c026d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052768"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>CBaseControlVideo. GetVideoFormat 方法

`GetVideoFormat`方法會抓取表示目前影片格式的影片範例。

## <a name="syntax"></a>語法


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的指標，其中包含目前的影片格式。

## <a name="remarks"></a>備註

若要透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)傳回和檢查特定資訊，物件必須知道目前的影片格式。 它會藉由呼叫衍生類別必須覆寫的純虛擬方法來取得此資訊。 下列 [**CBaseControlVideo**](cbasecontrolvideo.md) 成員函式會呼叫這個成員函式。

-   [**CBaseControlVideo::OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)
-   [**CBaseControlVideo：： get \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**CBaseControlVideo：：取得 \_ 位元速率**](cbasecontrolvideo-get-bitrate.md)
-   [**CBaseControlVideo：： get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)
-   [**CBaseControlVideo：： get \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)
-   [**CBaseControlVideo：： get \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)
-   [**CBaseControlVideo::GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**CBaseControlVideo::GetVideoSize**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




