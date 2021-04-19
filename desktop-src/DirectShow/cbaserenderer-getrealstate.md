---
description: GetRealState 方法會捕獲篩選狀態。
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: 'CBaseRenderer. GetRealState 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995226"
---
# <a name="cbaserenderergetrealstate-method"></a>CBaseRenderer. GetRealState 方法

`GetRealState`方法會捕獲篩選狀態。

## <a name="syntax"></a>語法


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBaseFilter：： m \_ 狀態**](cbasefilter-m-state.md)的值。 此值為 [**篩選準則 \_ 狀態**](/windows/win32/api/strmif/ne-strmif-filter_state) 列舉類型的成員。

## <a name="remarks"></a>備註

此方法提供更簡單的 [**CBaseRenderer：： >getstate**](cbaserenderer-getstate.md) 方法替代方式，以供內部使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




