---
description: CTransInPlaceFilter. GetPin 方法-GetPin 方法會抓取 pin。
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: 'CTransInPlaceFilter. GetPin 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084766"
---
# <a name="ctransinplacefiltergetpin-method"></a>CTransInPlaceFilter. GetPin 方法

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

這個方法會覆寫 [**CTransformFilter：： GetPin**](ctransformfilter-getpin.md) 方法。 第一次呼叫方法時，它會建立兩個圖釘。

這個方法不會遞增傳回的釘選上的參考計數，因此傳回的 pin 沒有未處理的參考計數。 如果呼叫端需要保留 pin 的參考，則應該在 pin 上呼叫 **IUnknown：： AddRef** 方法。

如果篩選使用預設的 [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) 和 [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) 釘選，您可能不需要覆寫這個方法。 但是，如果篩選使用擴充這些類別的釘選，您必須覆寫這個方法以建立該類型的釘選。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




