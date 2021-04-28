---
description: CBaseInputPin. NotifyAllocator 方法-NotifyAllocator 方法會指定連接的配置器。 這個方法會實 IMemInputPin：： NotifyAllocator 方法。
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: 'CBaseInputPin. NotifyAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c63e448d0cf2d287a441a4983f6a2e06bd9b8151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099713"
---
# <a name="cbaseinputpinnotifyallocator-method"></a>CBaseInputPin. NotifyAllocator 方法

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

傳回 S \_ OK。

## <a name="remarks"></a>備註

在 pin 連接期間，輸出釘選會選擇配置器，並呼叫這個方法來通知輸入 pin。 輸出 pin 可以使用 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法中所建議之輸入 pin 的配置器，也可以提供自己的配置器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




