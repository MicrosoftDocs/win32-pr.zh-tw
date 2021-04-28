---
description: CBaseOutputPin. DecideBufferSize 方法-DecideBufferSize 方法會設定緩衝區需求。
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: 'CBaseOutputPin. DecideBufferSize 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a76f058e2f9c07a344453db87046704e26280a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099526"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a>CBaseOutputPin. DecideBufferSize 方法

`DecideBufferSize`方法會設定緩衝區需求。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAlloc* 
</dt> <dd>

配置器的 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標。

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標，其中包含輸入釘選的緩衝區需求。 如果輸入的 pin 沒有任何需求，呼叫端應該在呼叫方法之前，先零出此結構的成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

在您的衍生類別中覆寫這個方法。 呼叫 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) 方法，以指定您的緩衝區需求。 一般而言，衍生類別會接受輸入 pin 的緩衝區需求，但不需要。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




