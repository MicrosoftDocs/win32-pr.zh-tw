---
description: GetCurrentPosition 方法會抓取目前的位置，相對於資料流程的總持續時間。 未實作。
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: 'CSourceSeeking. GetCurrentPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4069c8b1a83ade6897fedf87c16b89b1c63d3c1cef18d21a3bdbd594a3b2cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084055"
---
# <a name="csourceseekinggetcurrentposition-method"></a>CSourceSeeking. GetCurrentPosition 方法

方法會抓取 `GetCurrentPosition` 目前的位置，相對於資料流程的總持續時間。 未實作。

## <a name="syntax"></a>語法


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCurrent* 
</dt> <dd>

變數的指標，此變數會接收目前的位置，以目前時間格式的單位為單位。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 E \_ >notimpl。

## <a name="remarks"></a>備註

來源篩選準則通常不支援此方法。 相反地，轉譯器篩選會透過 [**CRendererPosPassThru**](crendererpospassthru.md) 類別來報告目前的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 




