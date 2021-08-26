---
description: CBasePin. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: 'CBasePin. CheckConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a91e936f13c76ed4d99d7c5048820777afa47c9a52c260bb7f34acb702cb777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916848"
---
# <a name="cbasepincheckconnect-method"></a>CBasePin. CheckConnect 方法

`CheckConnect`方法會判斷是否適合使用 pin 連接。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

指向其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                               | 描述                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                      | 成功。<br/>                           |
| <dl> <dt>**VFW \_ E \_ 不正確 \_ 方向**</dt> </dl> | Pin 方向不相容。<br/> |



 

## <a name="remarks"></a>備註

在連接程式開始時，這兩個圖釘都會呼叫這個方法。 連接的 pin 會從 [**CBasePin：：連線**](cbasepin-connect.md)方法內呼叫它，而接收的 pin 會從 [**CBasePin：： ReceiveConnection**](cbasepin-receiveconnection.md)方法中呼叫它。

您可以使用這個方法來判斷 *pPin* 參數所指定的 pin 是否適合用於連接。 如果兩個圖釘都 (輸入相同方向，或兩個輸出) 都有相同的方向，則基類會傳回錯誤。 衍生類別可以覆寫這個方法，以驗證 pin 中的其他功能。 例如， [**CBaseOutputPin**](cbaseoutputpin.md) 類別會查詢其 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的輸入 pin。

如果此方法失敗，連接就會失敗，而且 pin 會呼叫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法。 使用 **BreakConnect** 來釋放中取得的任何資源 `CheckConnect` 。 例如，如果 `CheckConnect` 呼叫 **QueryInterface** 方法，則 **BreakConnect** 必須釋放介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




