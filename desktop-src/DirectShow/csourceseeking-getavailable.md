---
description: CSourceSeeking. GetAvailable 方法-GetAvailable 方法會捕獲搜尋效率的範圍。 這個方法會實 IMediaSeeking：： GetAvailable 方法。
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: 'CSourceSeeking. GetAvailable 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae42efad42bf9f1e0df0f4f791f1e4e8abb76fe8252818a8e35eda4dd6e6b87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953747"
---
# <a name="csourceseekinggetavailable-method"></a>CSourceSeeking. GetAvailable 方法

`GetAvailable`方法會捕獲搜尋效率的範圍。 這個方法會實 [**IMediaSeeking：： GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pEarliest* 
</dt> <dd>

變數的指標，此變數會接收有效率搜尋的最早時間。 變數設定為零。

</dd> <dt>

*pLatest* 
</dt> <dd>

變數的指標，此變數會接收有效率搜尋的最新時間。 變數會設定為 [**CSourceSeeking：： m \_ rtDuration**](csourceseeking-m-rtduration.md) 成員變數的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




