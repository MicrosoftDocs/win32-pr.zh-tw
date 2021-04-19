---
description: NotifyAllocator 方法會指定連接的配置器。 這個方法會實 IMemInputPin：： NotifyAllocator 方法。
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: 'CTransInPlaceInputPin. NotifyAllocator 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74578243ce780e09d7435f9dd4b70bd9497e1e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993277"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a>CTransInPlaceInputPin. NotifyAllocator 方法

方法會指定連接的配置器 `NotifyAllocator` 。 這個方法會實 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAllocator* 
</dt> <dd>

配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。

</dd> <dt>

*bReadOnly* 
</dt> <dd>

旗標，指定此配置器的樣本是否為唯讀。 若 **為 TRUE**，則表示範例是唯讀的。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                               | Description                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | Success<br/>                   |
| <dl> <dt>**E \_ 失敗**</dt> </dl>    | 失敗<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數<br/> |



 

## <a name="remarks"></a>備註

篩選準則會嘗試針對兩個 pin 連接使用相同的配置器。

-   如果輸出針腳未連接，則輸入 pin 會自動接受配置器。 當輸出連接時，篩選器會重新連接輸入的 pin。 屆時，篩選器會再試一次使用單一配置器。
-   如果輸出連接已連線，則輸入插針會接受配置器。 輸出釘選也會使用相同的配置器。 它會呼叫 `NotifyAllocator` 下游輸入 pin。

先前的案例有下列例外狀況：

-   如果建議的配置器是唯讀的 (也就是說， *bReadOnly* 參數為 **TRUE**) 而且篩選準則需要修改範例，則篩選準則必須使用兩個不同的配置器。 在此情況下，如果上游篩選器打算使用下游篩選器的配置器，則方法會傳回 E \_ FAIL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceInputPin 類別**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




