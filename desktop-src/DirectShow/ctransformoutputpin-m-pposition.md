---
description: CTransformOutputPin：： m_pPosition 成員協助程式物件，以傳送上游的搜尋命令。
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'CTransformOutputPin：： m_pPosition 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bfa565d38fa982ea457da13ee9cf08a1d0f2fe8d5ba52ef3c5b86379fc02b509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538158"
---
# <a name="ctransformoutputpinm_pposition-member"></a>CTransformOutputPin：： m \_ pPosition 成員

要傳遞向上游傳遞搜尋命令的 Helper 物件。

## <a name="syntax"></a>語法


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>備註

第一次查詢 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 或 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面的 pin 時，它會建立並匯總 [**CPosPassThru**](cpospassthru.md) helper 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




