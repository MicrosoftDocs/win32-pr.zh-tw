---
description: 擁有線程的執行緒識別碼。
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'CCritSec：： m_currentOwner 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984847"
---
# <a name="ccritsecm_currentowner-member"></a>CCritSec：： m \_ currentOwner 成員

擁有線程的執行緒識別碼。

## <a name="syntax"></a>語法


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>備註

這個成員變數只會在基類的 debug 版本中定義。 [重要區段調試函數](critical-section-debugging-functions.md)會使用這個成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> </dl>

 

 




