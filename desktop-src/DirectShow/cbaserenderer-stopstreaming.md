---
description: 當篩選參數切換到執行中狀態時，StopStreaming 方法會停止串流。
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: 'CBaseRenderer. StopStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097ad9fd1548b709f7eb74a3e468c34c3b18a73621720e249a3c626c252c898d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016796"
---
# <a name="cbaserendererstopstreaming-method"></a>CBaseRenderer. StopStreaming 方法

`StopStreaming`當篩選參數切換到執行中狀態時，此方法會停止串流。

## <a name="syntax"></a>語法


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會呼叫 [**CBaseRenderer：： OnStopStreaming**](cbaserenderer-onstopstreaming.md) 方法。 該方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




