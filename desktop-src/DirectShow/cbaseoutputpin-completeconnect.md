---
description: CBaseOutputPin. CompleteConnect 方法-CompleteConnect 方法會完成輸入 pin 的連接。
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: 'CBaseOutputPin. CompleteConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9832ddc0a68936461f9fe9ee8a70a7da3227f93e9b0bc9f7328d4cc2f95c2f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823668"
---
# <a name="cbaseoutputpincompleteconnect-method"></a>CBaseOutputPin. CompleteConnect 方法

`CompleteConnect`方法會完成輸入 pin 的連接。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pReceivePin* 
</dt> <dd>

輸入釘選的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 方法。 它會呼叫 [**DecideAllocator**](cbaseoutputpin-decideallocator.md) 方法，以選取要用於此連接的記憶體配置器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




