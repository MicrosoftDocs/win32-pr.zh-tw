---
description: SetSink 方法會設定將接收品質訊息的 IQualityControl 物件。
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: 'CBaseVideoRenderer. SetSink 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977626"
---
# <a name="cbasevideorenderersetsink-method"></a>CBaseVideoRenderer. SetSink 方法

`SetSink`方法會設定將接收品質訊息的 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)物件。

## <a name="syntax"></a>語法


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*piqc* 
</dt> <dd>

應傳送通知之 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會在影片轉譯器上 [**執行 IQualityControl：： SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




