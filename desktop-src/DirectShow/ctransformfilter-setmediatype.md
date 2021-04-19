---
description: 當媒體類型是在其中一個篩選器的 pin 上設定時，就會呼叫 SetMediaType 方法。
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: 'CTransformFilter. SetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995024"
---
# <a name="ctransformfiltersetmediatype-method"></a>CTransformFilter. SetMediaType 方法

`SetMediaType`當媒體類型是在其中一個篩選器的釘選上設定時，就會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*direction* 
</dt> <dd>

[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，在篩選上指定釘選 (輸入或輸出) 。

</dd> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

當設定 pin 的媒體類型時， [**CTransformInputPin：： SetMediaType**](ctransforminputpin-setmediatype.md) 和 [**CTransformOutputPin：： SetMediaType**](ctransformoutputpin-setmediatype.md) 方法會呼叫這個方法。 這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




