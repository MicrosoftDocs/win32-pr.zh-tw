---
description: 指出篩選是否已傳送資料流程結束通知的旗標。
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'CTransformFilter：： m_bEOSDelivered 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978447"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>CTransformFilter：： m \_ bEOSDelivered 成員

指出篩選是否已傳送資料流程結束通知的旗標。

## <a name="syntax"></a>語法


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>備註

如果篩選在沒有輸入連接時暫停，則會傳送下游的結束資料流程通知，並將此旗標設定為 **TRUE**。 資料流程結束通知可確保下游篩選不會等候樣本。 請注意，篩選的 [**EndOfStream**](ctransformfilter-endofstream.md) 方法不會設定此旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




