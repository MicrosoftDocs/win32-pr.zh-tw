---
description: 資料流程的持續時間。 根據預設，值會設定為 CSourceSeeking：： m \_ rtStop 成員變數的值。
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'CSourceSeeking：： m_rtDuration 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6aa62a3cdf906a4e9666b7786c08e49fca250ef042d187902132410cc2f0abaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053968"
---
# <a name="csourceseekingm_rtduration-member"></a>CSourceSeeking：： m \_ rtDuration 成員

資料流程的持續時間。 根據預設，值會設定為 [**CSourceSeeking：： m \_ rtStop**](csourceseeking-m-rtstop.md) 成員變數的值。

## <a name="syntax"></a>語法


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>備註

存取此變數之前，請先保留 **m \_ pLock** 重要區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




