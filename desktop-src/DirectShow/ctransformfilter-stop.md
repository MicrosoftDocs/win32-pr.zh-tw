---
description: 停止篩選。 這個方法會實 IMediaFilter：： Stop 方法。
ms.assetid: e95537d6-b3ec-49a4-aa28-333d69eff3bb
title: 'CTransformFilter. Stop 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a7f7ea0f80095cd63f9708f12a42146260f2f8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999448"
---
# <a name="ctransformfilterstop-method"></a>CTransformFilter. Stop 方法

停止篩選。 這個方法會實 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Stop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

在這個方法解除這兩個配置器之後，它會呼叫 [**StopStreaming**](ctransformfilter-stopstreaming.md) 方法。 **StopStreaming** 方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




