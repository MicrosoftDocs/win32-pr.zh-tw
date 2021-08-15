---
description: 當篩選參數切換為暫停狀態時，就會呼叫 StartStreaming 方法。
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: 'CTransformFilter. StartStreaming 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d4a0c6e0e047819c208c8e592b971f013f9ed40d456a5b73ad64ea9153ddeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953427"
---
# <a name="ctransformfilterstartstreaming-method"></a>CTransformFilter. StartStreaming 方法

`StartStreaming`當篩選參數切換為暫停狀態時，就會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




