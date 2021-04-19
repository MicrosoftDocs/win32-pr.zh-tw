---
description: CAutoUsingOutputPin 類別會取得並釋放 CDynamicOutputPin 物件的存取權。
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: 'CAutoUsingOutputPin 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993615"
---
# <a name="cautousingoutputpin-class"></a>CAutoUsingOutputPin 類別

**CAutoUsingOutputPin** 類別會取得並釋放 [**CDynamicOutputPin**](cdynamicoutputpin.md)物件的存取權。

**CAutoUsingOutputPin** 具有下列類型的成員：



| 公用方法                                                           | Description                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)   | 函式方法。 取得指定之 pin 的存取權。 |
| [**~ CAutoUsingOutputPin**](cautousingoutputpin--cautousingoutputpin.md) | 函式方法。 取得指定之 pin 的存取權。  |



 

## <a name="remarks"></a>備註

在 [**CDynamicOutputPin**](cdynamicoutputpin.md)上呼叫特定方法時，呼叫端必須取得 pin 的存取權，然後釋放該存取權。 為了取得存取權，呼叫端會使用 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法。 若要釋放存取權，則會呼叫 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法。 **CAutoUsingOutputPin** 類別是一個 helper 類別，可在其函式和函式方法中處理這些工作。 下列程式碼範例顯示如何使用這個類別：


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[基類參考](base-class-reference.md)
</dt> </dl>

 

 




