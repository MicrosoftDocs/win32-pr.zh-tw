---
description: 清除方法會通知基類： pin 已啟動或停止排清。
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: 'CBaseStreamControl 方法 (Strmctl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981312"
---
# <a name="cbasestreamcontrolflushing-method"></a>CBaseStreamControl 方法

`Flushing`方法會通知基類： pin 已啟動或停止排清。

## <a name="syntax"></a>語法


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bInProgress* 
</dt> <dd>

指定布林值，指出是否正在清除釘選。 當 pin 開始排清作業時，使用值 **TRUE** ，當 pin 結束排清作業時，則 **為 FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

Pin 必須從其 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 和 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法中呼叫此方法。 在 **BeginFlush** 中指定 **TRUE** ，並在 **EndFlush** 中指定 **FALSE** 。

這個方法會導致 [**CBaseStreamControl：： CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) 方法停止等候。 當釘選時， **CheckStreamState** 一律會傳回資料流程 \_ 捨棄。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Strmctl (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseStreamControl 類別**](cbasestreamcontrol.md)
</dt> </dl>

 

 




