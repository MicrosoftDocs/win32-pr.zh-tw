---
description: InitAllocator 方法會建立記憶體配置器。
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: " (Amfilter 的 CBaseOutputPin.InitAllocator 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce1e8f8097ca88d0434f79c20e855d8b61798b5a1b0e32b6a38077e4c7aa1271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652458"
---
# <a name="cbaseoutputpininitallocator-method"></a>CBaseOutputPin.InitAllocator 方法

`InitAllocator`方法會建立記憶體配置器。

## <a name="syntax"></a>語法


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAlloc* 
</dt> <dd>

接收配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標的變數位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 [確定]，或從 **CoCreateInstance** 函數傳回錯誤碼。

## <a name="remarks"></a>備註

如果輸入 pin 未提供記憶體配置器， [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md) 方法就會呼叫這個方法來建立配置器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




