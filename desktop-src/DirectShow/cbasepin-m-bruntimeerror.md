---
description: 指出執行階段錯誤是否發生的旗標。
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'CBasePin：： m_bRunTimeError 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffc07a15f7c34744be52c5e2c7b5233e1885b58c5b9b7d078871277f8fc0efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823330"
---
# <a name="cbasepinm_bruntimeerror-member"></a>CBasePin：： m \_ bRunTimeError 成員

指出執行階段錯誤是否發生的旗標。

## <a name="syntax"></a>語法


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>備註

此旗標的預設值為 **FALSE**。 如果在串流處理期間發生執行階段錯誤，請將旗標設定為 **TRUE** 。 [**CBasePin：：非**](cbasepin-inactive.md)使用中方法會將旗標重設為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




