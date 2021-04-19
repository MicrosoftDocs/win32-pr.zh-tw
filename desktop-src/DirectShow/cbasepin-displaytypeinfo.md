---
description: DisplayTypeInfo 方法會在調試過程中顯示媒體類型資訊。
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: 'CBasePin. DisplayTypeInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977777"
---
# <a name="cbasepindisplaytypeinfo-method"></a>CBasePin. DisplayTypeInfo 方法

`DisplayTypeInfo`方法會在調試過程中顯示媒體類型資訊。

## <a name="syntax"></a>語法


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPin* 
</dt> <dd>

忽略。

</dd> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在 debug 組建中，這個方法會呼叫 [**DbgLog**](dbglog.md) 函數來顯示指定的媒體類型。 在零售組建中，此方法不會執行任何動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




