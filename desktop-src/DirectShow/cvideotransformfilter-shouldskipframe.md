---
description: ShouldSkipFrame 方法會判斷篩選是否應該卸載指定的範例。
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: 'CVideoTransformFilter. ShouldSkipFrame 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26a0c35be9914641abfa053cd1ee00f46bb09222aecbebc55d45900331a2ee81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075938"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>CVideoTransformFilter. ShouldSkipFrame 方法

`ShouldSkipFrame`方法會判斷篩選是否應該卸載指定的範例。

## <a name="syntax"></a>語法


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*針* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果篩選準則應該卸載此範例，則傳回 **TRUE** ; 如果篩選器應該處理此範例，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果符合下列條件，則此方法會傳回 **TRUE** ：

-   此範例具有時間戳記。
-   平均解碼時間至少為框架持續時間的25%。
-   轉譯器目前至少有一個最晚的框架，如同透過品質訊息所報告。
-   跳到下一個主要畫面格，並不會讓框架提早抵達一個以上的畫面格。

基於此計算的目的，篩選準則會在處理資料時記錄下列資訊：

-   過去20個框架的平均解碼時間 (**m \_ itrAvgDecode**) 
-   自最後一個主要畫面格之後的框架數目 (**m \_ nFramesSinceKeyFrame**) 
-   在主要畫面格 (**m \_ nKeyFramePeriod** 之間有多少個框架的估計) 

一旦篩選器卸載框架之後，它會繼續卸載框架，直到到達下一個主要畫面格為止。 如果這個方法傳回 **TRUE**，也會將 [**EC \_ 品質 \_ 變更**](ec-quality-change.md)事件傳送至篩選 Graph 管理員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Vtrans (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CVideoTransformFilter 類別**](cvideotransformfilter.md)
</dt> </dl>

 

 




