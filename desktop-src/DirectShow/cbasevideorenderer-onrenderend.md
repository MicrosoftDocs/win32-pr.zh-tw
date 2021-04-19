---
description: OnRenderEnd 方法會在轉譯時間因中斷而異的情況下執行平滑處理。
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: 'CBaseVideoRenderer. OnRenderEnd 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989255"
---
# <a name="cbasevideorendereronrenderend-method"></a>CBaseVideoRenderer. OnRenderEnd 方法

當轉譯 `OnRenderEnd` 時間因中斷而改變時，方法會執行平滑處理。

## <a name="syntax"></a>語法


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

媒體範例的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在繪製影像之後，就應該呼叫這個成員函式。

此成員函式會覆寫 [**CBaseRenderer：： OnRenderEnd**](cbaserenderer-onrenderend.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




