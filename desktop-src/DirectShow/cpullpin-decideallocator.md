---
description: DecideAllocator 方法會使用輸出圖釘來協調配置器。
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: 'CPullPin. DecideAllocator 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994816"
---
# <a name="cpullpindecideallocator-method"></a>CPullPin. DecideAllocator 方法

`DecideAllocator`方法會使用輸出圖釘來協調配置器。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAlloc* 
</dt> <dd>

輸入釘選配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標，或 **Null**。

</dd> <dt>

*pProps* 
</dt> <dd>

選用配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含輸入釘選的緩衝區需求。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則傳回錯誤碼。

## <a name="remarks"></a>備註

這個方法會呼叫 [**IAsyncReader：： RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) 方法來協調配置器。 它會將 *pAlloc* 參數直接傳遞給 **RequestAllocator** 方法。 如果 *pProps* 為非 **Null**，它會將 *pProps* 參數傳遞至 **RequestAllocator** ;否則，它會建立具有三個64K 緩衝區預設要求的配置器 **\_ 屬性** 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> <dt>

[**CPullPin：： Connect**](cpullpin-connect.md)
</dt> </dl>

 

 




