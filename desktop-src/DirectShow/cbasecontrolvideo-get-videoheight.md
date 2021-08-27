---
description: Get \_ VideoHeight 方法會抓取原生影片的高度。
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: 'CBaseControlVideo.get_VideoHeight 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a7ca4b87a9196a8b59ec00cdc0e458855fa1db4e1e8f7b5bfd233924475519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057078"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>CBaseControlVideo. 取得 \_ VideoHeight 方法

方法會抓取 `get_VideoHeight` 原生影片的高度。

## <a name="syntax"></a>語法


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVideoHeight* 
</dt> <dd>

原生影片高度的指標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR \_ ，如果沒有足夠的可用記憶體，則傳回 E OUTOFMEMORY。

## <a name="remarks"></a>備註

此成員函式會實 [**IBasicVideo：： get \_ VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) 方法。 它會呼叫純虛擬 [**CBaseControlVideo：： GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) ，以從衍生類別取出 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




