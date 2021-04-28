---
description: CBaseInputPin. GetAllocator 方法-GetAllocator 方法會抓取此 pin 提議的記憶體配置器。 這個方法會實 IMemInputPin：： GetAllocator 方法。
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: 'CBaseInputPin. GetAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72aaf6bb4c1ff8bf108086a8a42a618267c4bc06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099707"
---
# <a name="cbaseinputpingetallocator-method"></a>CBaseInputPin. GetAllocator 方法

方法會抓取 `GetAllocator` 此 pin 提議的記憶體配置器。 這個方法會實 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAllocator* 
</dt> <dd>

接收配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標的變數位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 [確定]，或從 **CoCreateInstance** 函數傳回錯誤碼。

## <a name="remarks"></a>備註

這個方法會建立 [**CMemAllocator**](cmemallocator.md) 物件。 如果您的篩選器使用來自下游 pin 或自訂配置器的配置器，請覆寫這個方法。

如果方法成功，則 **IMemAllocator** 介面具有未處理的參考計數。 當您完成時，請務必放開。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




