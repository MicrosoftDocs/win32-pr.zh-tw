---
description: BeginFlush 方法會開始進行清除作業。
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: 'CTransformFilter. BeginFlush 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982547"
---
# <a name="ctransformfilterbeginflush-method"></a>CTransformFilter. BeginFlush 方法

`BeginFlush`方法會開始清除作業。

## <a name="syntax"></a>語法


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

在排清作業開始時，輸入釘選的 [**CTransformInputPin：： BeginFlush**](ctransforminputpin-beginflush.md) 方法會呼叫這個方法。 這個方法會將 `BeginFlush` 呼叫傳遞給下游。

如果衍生類別使用背景工作執行緒來傳遞範例，則在排清作業期間，應該捨棄任何已排入佇列的資料。 可以在 `BeginFlush` 方法中或在 [**EndFlush**](ctransformfilter-endflush.md) 方法中完成。 不過請注意，的呼叫 `BeginFlush` 不會與資料流程處理執行緒同步處理。 如果 `BeginFlush` 方法捨棄佇列資料，則篩選準則必須小心，不要在 `BeginFlush` 和 **EndFlush** 呼叫之間處理任何其他資料。 如需詳細資訊，請參閱 [篩選開發人員的](data-flow-for-filter-developers.md)資料流程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




