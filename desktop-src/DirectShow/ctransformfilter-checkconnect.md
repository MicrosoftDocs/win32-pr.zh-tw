---
description: CTransformFilter. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: 'CTransformFilter. CheckConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a148e9edbc1cef42ecc2d1158dd18afcc908cf4d7549912b52f363aaa54cedb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953627"
---
# <a name="ctransformfiltercheckconnect-method"></a>CTransformFilter. CheckConnect 方法

`CheckConnect`方法會判斷是否適合使用 pin 連接。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dir* 
</dt> <dd>

[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定篩選上的哪個圖釘正在進行連接。

</dd> <dt>

*pPin* 
</dt> <dd>

此連接嘗試中其他 pin 的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CTransformInputPin：： CheckConnect**](ctransforminputpin-checkconnect.md)和 [**CTransformOutputPin：： CheckConnect**](ctransformoutputpin-checkconnect.md)方法會在 pin 連接處理期間呼叫這個方法。 這個方法不會在基類中執行任何動作。 衍生的類別可以覆寫它。 例如，衍生類別可能會查詢特定介面的其他 pin。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




