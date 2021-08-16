---
description: 指出篩選目前是否正在卸載框架的布林值。 如果這個值為 TRUE，則篩選會繼續卸載框架，直到到達下一個主要畫面格，或直到它在沒有主要畫面格的資料列中收到30個差異框架為止。
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'CVideoTransformFilter：： m_bSkipping 成員 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f865bdc707b206a8528413a357a4e14bcfe88fff813e1f62a44d30e6f4843ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821913"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>CVideoTransformFilter：： m \_ bSkipping 成員

指出篩選目前是否正在卸載框架的布林值。 如果這個值為 **TRUE**，則篩選會繼續卸載框架，直到到達下一個主要畫面格，或直到它在沒有主要畫面格的資料列中收到30個差異框架為止。

## <a name="syntax"></a>Syntax


```C++
BOOL m_bSkipping;
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

 

 




