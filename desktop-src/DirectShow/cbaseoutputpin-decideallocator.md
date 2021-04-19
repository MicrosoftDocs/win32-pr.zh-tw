---
description: DecideAllocator 方法會選取記憶體配置器。
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: 'CBaseOutputPin. DecideAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990064"
---
# <a name="cbaseoutputpindecideallocator-method"></a>CBaseOutputPin. DecideAllocator 方法

`DecideAllocator`方法會選取記憶體配置器。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

輸入釘選 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的指標。

</dd> <dt>

*pAlloc* 
</dt> <dd>

接收配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面指標的變數位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

在 pin 連線程式結束時，會呼叫這個方法。 它會執行下列步驟：

1.  呼叫 [**IMemInputPin：： GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) 方法，以取得輸入釘選的緩衝區需求（如果有的話）。
2.  呼叫 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法，以從輸入 pin 要求配置器。 如果輸入 pin 未提供配置器，輸出釘選會藉由呼叫 [**CBaseOutputPin：： InitAllocator**](cbaseoutputpin-initallocator.md) 類別方法來建立一個配置器。
3.  呼叫 [**CBaseOutputPin：:D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) 類別方法，它會設定配置器屬性。 這是純虛擬方法;衍生的類別必須加以執行。
4.  呼叫 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 方法，這會通知所使用配置器的輸入 pin。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




