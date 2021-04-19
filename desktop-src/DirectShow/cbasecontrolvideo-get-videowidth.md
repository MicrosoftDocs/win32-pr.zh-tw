---
description: Get \_ VideoWidth 方法會抓取原生影片的寬度。
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: 'CBaseControlVideo.get_VideoWidth 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984480"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a>CBaseControlVideo. 取得 \_ VideoWidth 方法

方法會抓取 `get_VideoWidth` 原生影片的寬度。

## <a name="syntax"></a>語法


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVideoWidth* 
</dt> <dd>

原生影片的寬度指標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR \_ ，如果沒有足夠的可用記憶體，則傳回 E OUTOFMEMORY。

## <a name="remarks"></a>備註

此成員函式會實 [**IBasicVideo：： get \_ VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) 方法。 它會呼叫純虛擬 [**CBaseControlVideo：： GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) ，以從衍生類別取出 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




