---
description: EndFlush 方法會結束清除作業。 這個方法會覆寫 CTransformFilter：： EndFlush 方法。
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: 'CVideoTransformFilter. EndFlush 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359229e690715667d7bbfbe3d3a9134f41f5af9febc185885e08cde7d986896e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155872"
---
# <a name="cvideotransformfilterendflush-method"></a>CVideoTransformFilter. EndFlush 方法

`EndFlush`方法會結束清除作業。 這個方法會覆寫 [**CTransformFilter：： EndFlush**](ctransformfilter-endflush.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 [確定]，否則傳回錯誤碼。

## <a name="remarks"></a>備註

這個方法會重設所有篩選器的內部效能度量。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Vtrans (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CVideoTransformFilter 類別**](cvideotransformfilter.md)
</dt> </dl>

 

 




