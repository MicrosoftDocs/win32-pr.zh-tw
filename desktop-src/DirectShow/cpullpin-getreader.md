---
description: System.diagnostics.symbolstore.isymbolbinder1.getreader 方法會傳回輸出釘選的 IAsyncReader 介面指標。
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: 'CPullPin. System.diagnostics.symbolstore.isymbolbinder1.getreader 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996003"
---
# <a name="cpullpingetreader-method"></a>CPullPin. System.diagnostics.symbolstore.isymbolbinder1.getreader 方法

方法會傳回 `GetReader` 輸出釘選 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的指標。

## <a name="syntax"></a>語法


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的指標。

## <a name="remarks"></a>備註

傳回的介面具有未處理的參考計數。 呼叫端必須釋放介面。

在呼叫 **AddRef** 之前，方法不會檢查介面指標的值，因此，除非您已成功呼叫 [**CPullPin：： Connect**](cpullpin-connect.md) 方法，否則請不要呼叫這個方法。 否則，介面指標可能是 **Null** ，而且呼叫 **AddRef** 將會擲回例外狀況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




