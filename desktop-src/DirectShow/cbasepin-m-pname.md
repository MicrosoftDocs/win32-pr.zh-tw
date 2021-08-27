---
description: Pin 名稱。
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'CBasePin：： m_pName 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: d118ed76650b9ea580c0143ff4334a480d110c4a9d9531a23dda60c05c614630
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052678"
---
# <a name="cbasepinm_pname-member"></a>CBasePin：： m \_ pName 成員

Pin 名稱。

## <a name="syntax"></a>語法


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>備註

[**CBasePin：： QueryPinInfo**](cbasepin-querypininfo.md)方法會將此字串傳回為 pin 名稱，而 [**CBasePin：： QueryId**](cbasepin-queryid.md)方法會將其傳回做為 pin 識別碼。 但一般而言，pin 名稱和 pin 識別碼不需要相同的名稱。 Pin 識別碼會用於圖形持續性。 如需詳細資訊，請參閱 [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Amfilter (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




