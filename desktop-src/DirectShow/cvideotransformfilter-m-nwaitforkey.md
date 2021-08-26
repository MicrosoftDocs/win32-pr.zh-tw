---
description: 要卸載之 delta 框架的目前最大數目。
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'CVideoTransformFilter：： m_nWaitForKey 成員 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83cb78b233385e502d6508212492c54865aca28990ae079e4bf588776bd83fe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998538"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>CVideoTransformFilter：： m \_ nWaitForKey 成員

要卸載之 delta 框架的目前最大數目。 雖然此變數大於零，但是篩選會捨棄框架，直到到達主要畫面格為止。 針對每個已卸載的框架，篩選器會將此變數遞減一，以防止篩選器卸載過多的畫面格數目。 在沒有主要畫面格的資料列中有30個差異框架之後，篩選器會再次開始傳遞框架。

## <a name="syntax"></a>Syntax


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Vtrans (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CVideoTransformFilter 類別**](cvideotransformfilter.md)
</dt> </dl>

 

 




