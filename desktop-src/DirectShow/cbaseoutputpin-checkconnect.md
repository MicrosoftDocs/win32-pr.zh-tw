---
description: CBaseOutputPin. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: 'CBaseOutputPin. CheckConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ea5ad32de18046f3d23145d82e971391c3e304c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096186"
---
# <a name="cbaseoutputpincheckconnect-method"></a>CBaseOutputPin. CheckConnect 方法

`CheckConnect`方法會判斷是否適合使用 pin 連接。

## <a name="syntax"></a>語法


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

輸入釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                               | Description                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                      | 成功。<br/>                                                         |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>             | 輸入 pin 不支援 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)。<br/> |
| <dl> <dt>**VFW \_ E \_ 不正確 \_ 方向**</dt> </dl> | Pin 方向不相容。<br/>                               |



 

## <a name="remarks"></a>備註

這個方法會呼叫基類 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法，然後查詢其 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的輸入釘選。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




