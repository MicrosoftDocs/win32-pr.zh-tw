---
description: ReconnectPin 方法會中斷現有的 pin 連線，並使用指定的媒體類型將它重新連接到相同的 pin。
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: 'CBaseFilter. ReconnectPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39cef0ac5a0a7c4f186b8eae90a96a8e26fbf886f819dc7562cb7d8df4e087e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659718"
---
# <a name="cbasefilterreconnectpin-method"></a>CBaseFilter. ReconnectPin 方法

`ReconnectPin`方法會中斷現有的 pin 連線，並使用指定的媒體類型將它重新連接到相同的 pin。

## <a name="syntax"></a>語法


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標，或 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                   | 描述                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | [**m \_ pGraph**](cbasefilter-m-pgraph.md) 成員變數為 **Null**。<br/> |



 

## <a name="remarks"></a>備註

這個方法會在篩選圖形管理員上呼叫 [**IFilterGraph2：： ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) 方法。 如果無法使用 [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) 介面，方法會呼叫 [**IFilterGraph：： Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




