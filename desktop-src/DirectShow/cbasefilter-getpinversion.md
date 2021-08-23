---
description: GetPinVersion 方法會在此篩選器上抓取一組釘選的版本號碼。
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: 'CBaseFilter. GetPinVersion 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a40890ce40e75ebea9f7dd10edb78572eb865ea5f94cd1ec674c082d6df8c631
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640458"
---
# <a name="cbasefiltergetpinversion-method"></a>CBaseFilter. GetPinVersion 方法

`GetPinVersion`方法會在此篩選器上抓取一組釘選的版本號碼。

## <a name="syntax"></a>語法


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBaseFilter：： m \_ PinVersion**](cbasefilter-m-pinversion.md) 成員變數。

## <a name="remarks"></a>備註

**CBaseFilter** 函式會將 pin 版本初始化為1。 在基類中，此數位永遠不會變更。 如果篩選動態建立或終結 pin，則每當 pin 變更時，就應該遞增 pin 版本。 若要遞增版本號碼，請呼叫 [**CBaseFilter：： IncrementPinVersion**](cbasefilter-incrementpinversion.md) 方法。

Pin 列舉值物件是由 [**CEnumPins**](cenumpins.md) 類別所執行，它會使用 pin 版本將本身與篩選準則保持同步。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




