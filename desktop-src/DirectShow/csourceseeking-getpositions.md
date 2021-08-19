---
description: GetPositions 方法會抓取目前的位置和停止位置。 這個方法會實 IMediaSeeking：： GetPositions 方法。
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: 'CSourceSeeking. GetPositions 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b6f52d8d8b30a28d942d4395a465b9c7c49d0a23020ad212c81eb170d20ca0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073333"
---
# <a name="csourceseekinggetpositions-method"></a>CSourceSeeking. GetPositions 方法

方法會抓取 `GetPositions` 目前的位置和停止位置。 這個方法會實 [**IMediaSeeking：： GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCurrent* 
</dt> <dd>

接收開始位置之變數的指標。

</dd> <dt>

*pStop* 
</dt> <dd>

接收停用位置之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

針對 *pCurrent* 參數，這個方法會傳回 [**CSourceSeeking：： m \_ rtStart**](csourceseeking-m-rtstart.md) 成員變數的值，其代表最新的搜尋時間，而不是目前的串流位置。 不過，當應用程式透過篩選圖形管理員呼叫 **IMediaSeeking：： GetPositions** 時，這些值通常來自轉譯器篩選器，而不是來源篩選。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




