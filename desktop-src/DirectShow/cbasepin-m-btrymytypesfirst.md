---
description: 旗標，指出 pin 是否先嘗試其慣用的媒體類型，再接收 pin。
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'CBasePin：： m_bTryMyTypesFirst 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df94a95783d15c09fd53bd8659db71f2ce0b1aefe5d855fef5f5a03e71445493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158369"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>CBasePin：： m \_ bTryMyTypesFirst 成員

旗標，指出 pin 是否先嘗試其慣用的媒體類型，再接收 pin。

## <a name="syntax"></a>語法


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>備註

此旗標的預設值為 **FALSE**。 如果旗標為 **TRUE**， [**CBasePin：： AgreeMediaType**](cbasepin-agreemediatype.md) 方法會反轉嘗試媒體類型的順序。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




