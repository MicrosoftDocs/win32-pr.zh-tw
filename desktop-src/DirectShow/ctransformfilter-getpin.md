---
description: GetPin 方法會抓取 pin。
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: 'CTransformFilter. GetPin 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 30567db84eefd5471dbbe1fbd2d2e5ed64514ba2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979514"
---
# <a name="ctransformfiltergetpin-method"></a>CTransformFilter. GetPin 方法

方法會抓取 `GetPin` pin。

## <a name="syntax"></a>語法


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

指定之 pin 的編號，從零開始編制索引。 在此篩選準則中，pin 0 是輸入 pin，而 pin 1 是輸出 pin。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**CBasePin**](cbasepin.md) 物件的指標，該物件會執行釘選，如果方法失敗，則為 **Null** 。

## <a name="remarks"></a>備註

這個方法會實作為純虛擬 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 方法。 第一次呼叫方法時，它會建立兩個圖釘。

這個方法不會遞增傳回的釘選上的參考計數，因此傳回的 pin 沒有未處理的參考計數。 如果呼叫端需要保留 pin 的參考，則應該在 pin 上呼叫 **IUnknown：： AddRef** 方法。

如果篩選使用預設的 [**CTransformInputPin**](ctransforminputpin.md) 和 [**CTransformOutputPin**](ctransformoutputpin.md) 釘選，您可能不需要覆寫這個方法。 但是，如果篩選使用擴充這些類別的釘選，您必須覆寫這個方法以建立該類型的釘選。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




