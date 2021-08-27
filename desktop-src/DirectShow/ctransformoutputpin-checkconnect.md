---
description: CTransformOutputPin. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: 'CTransformOutputPin. CheckConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b85c2197cf65465441387ecc661af71e0ddfa7ca912c3296ddee543d11c4784
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086988"
---
# <a name="ctransformoutputpincheckconnect-method"></a>CTransformOutputPin. CheckConnect 方法

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

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | 描述                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                                 |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 篩選的輸入 pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseOutputPin：： CheckConnect**](cbaseoutputpin-checkconnect.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： CheckConnect**](ctransformfilter-checkconnect.md) 方法，它會 \_ 在基類中傳回 s OK。 衍生類別可以覆寫 **CTransformFilter：： CheckConnect** 方法，以執行額外的檢查。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




