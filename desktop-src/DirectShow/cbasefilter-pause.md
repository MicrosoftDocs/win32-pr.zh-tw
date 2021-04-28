---
description: CBaseFilter： pause 方法： Pause 方法會暫停篩選。 這個方法會實 IMediaFilter：:P ause 方法。
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: 'CBaseFilter： Pause 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120086"
---
# <a name="cbasefilterpause-method"></a>CBaseFilter. Pause 方法

`Pause`方法會暫停篩選。 這個方法會實 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Pause();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會在每個篩選器的連接釘上呼叫 [**CBasePin：： Active**](cbasepin-active.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




