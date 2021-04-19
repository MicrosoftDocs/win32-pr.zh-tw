---
description: 非使用中的方法會通知 pin，篩選已不再有效。 這個方法會覆寫 CBasePin：：非使用中的方法。 如果串流執行緒為使用中，此方法會停止它，並等候執行緒結束。
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: CSourceStream (Source. h) 的非使用中方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983042"
---
# <a name="csourcestreaminactive-method"></a>CSourceStream 方法

`Inactive`方法會通知 pin，篩選已不再有效。 這個方法會覆寫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中的方法。 如果串流執行緒為使用中，此方法會停止它，並等候執行緒結束。

## <a name="syntax"></a>語法


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




