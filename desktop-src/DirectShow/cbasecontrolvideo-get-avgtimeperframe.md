---
description: Get \_ AvgTimePerFrame 方法會抓取每個畫面格的平均時間。
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: 'CBaseControlVideo.get_AvgTimePerFrame 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989794"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a>CBaseControlVideo. 取得 \_ AvgTimePerFrame 方法

方法會抓取 `get_AvgTimePerFrame` 每個框架的平均時間。

## <a name="syntax"></a>語法


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAvgTimePerFrame* 
</dt> <dd>

每個框架的平均時間指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR \_ ，如果沒有足夠的可用記憶體，則傳回 E OUTOFMEMORY。

## <a name="remarks"></a>備註

此成員函式會實 [**IBasicVideo：： get \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) 方法。 它會呼叫純虛擬 [**CBaseControlVideo：： GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) 成員函式，以從衍生類別取出 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




