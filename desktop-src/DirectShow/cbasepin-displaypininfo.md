---
description: DisplayPinInfo 方法會在調試過程中追蹤 pin 連接。
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: 'CBasePin. DisplayPinInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98930ec48d3daa13d6ae463b38ce1ae62d745de9fae65915dcabcedf3cd673aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916468"
---
# <a name="cbasepindisplaypininfo-method"></a>CBasePin. DisplayPinInfo 方法

`DisplayPinInfo`方法會在調試過程中追蹤 pin 連接。

## <a name="syntax"></a>語法


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pReceivePin* 
</dt> <dd>

接收的釘選指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在 debug 組建中，這個方法會呼叫 [**DbgLog**](dbglog.md) 函數來追蹤連接嘗試。 在零售組建中，此方法不會執行任何動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




