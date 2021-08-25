---
description: 中斷連接方法會中斷與輸出 pin 的連接。
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: 'CPullPin 連接方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0491bfba7e5b739a2b46674cc2f6506017810d4f1e51693d4478720c67a4a4da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055068"
---
# <a name="cpullpindisconnect-method"></a>CPullPin 中斷方法

方法會將 `Disconnect` 連接與輸出釘選中斷。

## <a name="syntax"></a>語法


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會中斷 [**CPullPin：：連線**](cpullpin-connect.md)方法中所做的任何連接。 在您的 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) 方法內呼叫這個方法。  (如果您的 pin 衍生自 [**CBasePin**](cbasepin.md)，請覆寫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 以呼叫這個方法。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




