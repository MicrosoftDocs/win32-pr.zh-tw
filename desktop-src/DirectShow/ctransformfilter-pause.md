---
description: CTransformFilter： pause 方法： Pause 方法會暫停篩選。 這個方法會實 IMediaFilter：:P ause 方法。
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: 'CTransformFilter： Pause 方法 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 51584bc38c49345f6bb1d940aed24a052e9a4f9cd05fc2dc84246a6ba1168fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953497"
---
# <a name="ctransformfilterpause-method"></a>CTransformFilter. Pause 方法

`Pause`方法會暫停篩選。 這個方法會實 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Pause();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會呼叫 [**StartStreaming**](ctransformfilter-startstreaming.md) 方法。 **StartStreaming** 方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




