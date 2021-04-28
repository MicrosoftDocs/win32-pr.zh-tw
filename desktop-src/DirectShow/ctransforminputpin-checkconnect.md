---
description: CTransformInputPin. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: 'CTransformInputPin. CheckConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e981254677c2e0a361a0a21f125f734ff1403db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095086"
---
# <a name="ctransforminputpincheckconnect-method"></a>CTransformInputPin. CheckConnect 方法

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

輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                               | Description                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                      | Success<br/>             |
| <dl> <dt>**VFW \_ E \_ 不正確 \_ 方向**</dt> </dl> | 錯誤的 pin 方向<br/> |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： CheckConnect**](ctransformfilter-checkconnect.md) 方法，它會 \_ 在基類中傳回 s OK。 衍生類別可以覆寫 **CTransformFilter：： CheckConnect** 方法，以執行額外的檢查。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




