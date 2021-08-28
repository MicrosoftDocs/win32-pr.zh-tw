---
description: CTransformFilter. EndFlush 方法-EndFlush 方法會結束清除作業。
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: 'CTransformFilter. EndFlush 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 593ce39dbba6ccf90838b4847bb0a548b67e4785bb21d3f299882e1eecdf8394
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083908"
---
# <a name="ctransformfilterendflush-method"></a>CTransformFilter. EndFlush 方法

`EndFlush`方法會結束清除作業。

## <a name="syntax"></a>語法


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

在清除作業結束時，輸入釘選的 [**CTransformInputPin：： EndFlush**](ctransforminputpin-endflush.md) 方法會呼叫這個方法。 這個方法會將 `EndFlush` 呼叫傳遞給下游。

如果衍生類別使用背景工作執行緒來傳遞範例，則必須先捨棄所有已排入佇列的資料，然後再傳送 `EndFlush` 呼叫下游。 如需詳細資訊，請參閱[篩選開發人員的資料 Flow](data-flow-for-filter-developers.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




