---
description: Get \_ AvgFrameRate 方法會計算並取得平均畫面播放速率。
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: 'CBaseVideoRenderer.get_AvgFrameRate 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79aab0677cfd5cba5f6a889519e0c12ed2236d8f82eca28b3fa7b227b941b2b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658781"
---
# <a name="cbasevideorendererget_avgframerate-method"></a>CBaseVideoRenderer. 取得 \_ AvgFrameRate 方法

`get_AvgFrameRate`方法會計算並取得平均畫面播放速率。

## <a name="syntax"></a>語法


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*piAvgFrameRate* 
</dt> <dd>

串流開始之後每秒的畫面格數指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實 [**IQualProp：： get \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




