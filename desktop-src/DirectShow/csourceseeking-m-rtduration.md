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
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995785"
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

 

 




