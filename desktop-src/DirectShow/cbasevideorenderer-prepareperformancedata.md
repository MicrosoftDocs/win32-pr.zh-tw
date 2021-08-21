---
description: PreparePerformanceData 方法會設定 \_ 目前框架的 m trLate 和 m \_ trFrame 值。
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: 'CBaseVideoRenderer. PreparePerformanceData 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8cb276b37e64b6bb34751ed2d034666f7ceeddd90d8e52e47b2a1fca499ff9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658332"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>CBaseVideoRenderer. PreparePerformanceData 方法

`PreparePerformanceData`方法會設定目前框架的 **m \_ trLate** 和 **m \_ trFrame** 值。

## <a name="syntax"></a>語法


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*trLate* 
</dt> <dd>

值，指出取樣超過其到期時間的延遲時間（以參考時間單位為單位）。

</dd> <dt>

*trFrame* 
</dt> <dd>

在參考時間單位中的幀時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此成員函式會將 **m \_ trLate** 設為 *trLate* 的值，並將 **m \_ trFrame** 設定為 *trFrame* 的值。

從 [**CBaseVideoRenderer：： OnRenderStart**](cbasevideorenderer-onrenderstart.md)或 [**CBaseVideoRenderer：： OnDirectRender**](cbasevideorenderer-ondirectrender.md)呼叫 [**CBaseVideoRenderer：： RecordFrameLateness**](cbasevideorenderer-recordframelateness.md)成員函式時，它會傳遞 **m \_ trLate** 和 **m \_ trFrame** 的值來更新統計資料。 `PreparePerformanceData` 從 [**CBaseVideoRenderer：： OnWaitEnd**](cbasevideorenderer-onwaitend.md) 呼叫，以設定這些資料成員值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




