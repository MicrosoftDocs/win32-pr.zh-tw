---
description: 搜尋功能。
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'CSourceSeeking：： m_dwSeekingCaps 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992588"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>CSourceSeeking：： m \_ dwSeekingCaps 成員

搜尋功能。

## <a name="syntax"></a>語法


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>備註

依預設，此值會設定為下列旗標的位元組合：

-   \_搜尋 \_ CanSeekForwards
-   \_搜尋 \_ CanSeekBackwards
-   \_搜尋 \_ CanSeekAbsolute
-   \_搜尋 \_ CanGetStopPos
-   \_搜尋 \_ CanGetDuration

如果篩選支援一組不同的功能，請覆寫此值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




