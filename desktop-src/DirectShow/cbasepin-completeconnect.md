---
description: CompleteConnect 方法會完成與另一個 pin 的連接。
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: 'CBasePin. CompleteConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990093"
---
# <a name="cbasepincompleteconnect-method"></a>CBasePin. CompleteConnect 方法

`CompleteConnect`方法會完成與另一個 pin 的連接。

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

指向其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

在連接程式結束時，會在這兩個 pin 上呼叫這個方法。 連接的 pin 會從 [**CBasePin：： Connect**](cbasepin-connect.md) 方法內呼叫它，而接收的 pin 會從 [**CBasePin：： ReceiveConnection**](cbasepin-receiveconnection.md) 方法中呼叫它。

在基類中，此方法只會傳回 S \_ OK。 如果衍生類別具有完成連接的任何需求，則應該覆寫這個方法。 例如， [**CBaseOutputPin**](cbaseoutputpin.md) 類別會使用此方法來決定記憶體配置器。

如果此方法失敗，整體連接嘗試也會失敗，而且 pin 會與接收的 pin 中斷連線。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




