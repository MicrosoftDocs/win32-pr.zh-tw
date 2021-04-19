---
description: 建立映射的記憶體複本。
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: 'CBaseControlVideo. CopyImage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990613"
---
# <a name="cbasecontrolvideocopyimage-method"></a>CBaseControlVideo. CopyImage 方法

建立映射的記憶體複本。

## <a name="syntax"></a>語法


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

包含影片影像之範例的指標。

</dd> <dt>

*pVideoInfo* 
</dt> <dd>

代表影片影像的格式指標。

</dd> <dt>

*pBufferSize* 
</dt> <dd>

輸出緩衝區大小的指標。

</dd> <dt>

*pVideoImage* 
</dt> <dd>

輸出緩衝區的指標。

</dd> <dt>

*pSourceRect* 
</dt> <dd>

來源影片矩形的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *pVideoImage* 參數為 **Null**，則會以輸出緩衝區儲存影像所需的位元組數填入 *pBufferSize* 參數。 如果傳入的緩衝區太小，或成員函式無法配置足夠的記憶體，則成員函式會傳回 E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

成員函式會從範例抓取影像，並將它複製到輸出緩衝區。 複製到輸出緩衝區的影片區段會反映透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面設定的來源矩形 (但不會反映) 的目的地矩形。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




