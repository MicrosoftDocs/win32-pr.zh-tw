---
description: CBaseInputPin. BreakConnect 方法-BreakConnect 方法會釋放連接的 pin。
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: 'CBaseInputPin. BreakConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 625eab8cc070240d79456bff919317f884826fc6d14c26055b68de40aba4c969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403487"
---
# <a name="cbaseinputpinbreakconnect-method"></a>CBaseInputPin. BreakConnect 方法

`BreakConnect`方法會從連接釋放 pin。

## <a name="syntax"></a>語法


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法。 它會解除配置器，並釋放 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。

如果您覆寫這個方法，請從您的覆寫方法中呼叫基類方法。 否則，您可能會造成記憶體流失。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




