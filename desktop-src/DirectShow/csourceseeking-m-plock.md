---
description: 重要區段物件的指標。
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'CSourceSeeking：： m_pLock 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994758"
---
# <a name="csourceseekingm_plock-member"></a>CSourceSeeking：： m \_ pLock 成員

重要區段物件的指標。 `CSourceSeeking`類別會使用此重要區段來同步處理開始和停止時間、持續時間和速率變數的存取。 此變數會在函式方法中初始化。請參閱 [**CSourceSeeking：： CSourceSeeking**](csourceseeking-csourceseeking.md)。

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




