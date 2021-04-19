---
description: BreakConnect 方法會從連接釋放 pin。
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: 'CTransformFilter. BreakConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994613"
---
# <a name="ctransformfilterbreakconnect-method"></a>CTransformFilter. BreakConnect 方法

`BreakConnect`方法會從連接釋放 pin。

## <a name="syntax"></a>語法


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dir* 
</dt> <dd>

[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定 (輸入或輸出) 中斷的 pin 連接。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

當 pin 連接中斷時， [**CTransformInputPin：： BreakConnect**](ctransforminputpin-breakconnect.md) 和 [**CTransformOutputPin：： BreakConnect**](ctransformoutputpin-breakconnect.md) 方法會呼叫這個方法。 這個方法不會在基類中執行任何動作。 如果您覆寫 [**CheckConnect**](ctransformfilter-checkconnect.md) 方法，請覆寫此方法以釋放在 **CheckConnect** 方法中取得的任何資源，包括介面指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




