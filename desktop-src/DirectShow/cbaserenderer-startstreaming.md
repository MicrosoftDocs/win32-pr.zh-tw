---
description: 當篩選參數切換到執行中狀態時，StartStreaming 方法會啟動串流處理。
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: 'CBaseRenderer. StartStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8a9a70d403c4251c3250fc4d6f19c985a1546ea563a0d1bfe50ef7d7c6cfeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157485"
---
# <a name="cbaserendererstartstreaming-method"></a>CBaseRenderer. StartStreaming 方法

`StartStreaming`當篩選參數切換到執行中狀態時，此方法會起始資料流程處理。

## <a name="syntax"></a>語法


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

如果篩選器有範例，則會排程轉譯的範例。 否則，如果有暫止的資料流程結束通知，篩選準則會將 [**EC \_ 完成**](ec-complete.md) 事件傳送至篩選圖形管理員。

這個方法會呼叫 [**CBaseRenderer：： OnStartStreaming**](cbaserenderer-onstartstreaming.md) 方法。 該方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




