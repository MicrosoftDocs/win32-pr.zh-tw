---
description: SetReconnectWhenActive 方法會指定 pin 是否支援動態重新連接。
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: 'CBasePin. SetReconnectWhenActive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992776"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>CBasePin. SetReconnectWhenActive 方法

`SetReconnectWhenActive`方法會指定 pin 是否支援動態重新連接。

## <a name="syntax"></a>語法


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bCanReconnect* 
</dt> <dd>

指定 pin 是否可動態重新連接的布林值。 若 **為 TRUE**，則 pin 可以動態重新連接。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

根據預設，您必須先停止篩選，才能重新連接其任何 pin。 如果在篩選準則為使用中時，pin 可以重新連接，請以 **TRUE** 的值呼叫此方法。 如需詳細資訊，請參閱 [動態圖形建築物](dynamic-graph-building.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




