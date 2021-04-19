---
description: 停止時間。 根據預設，值會設定為非常大的數位。 衍生的類別可以重設其函式中的值，或初始化篩選時的值。
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'CSourceSeeking：： m_rtStop 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981309"
---
# <a name="csourceseekingm_rtstop-member"></a>CSourceSeeking：： m \_ rtStop 成員

停止時間。 根據預設，值會設定為非常大的數位。 衍生的類別可以重設其函式中的值，或初始化篩選時的值。

## <a name="syntax"></a>語法


```C++
CRefTime m_rtStop;
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

 

 




