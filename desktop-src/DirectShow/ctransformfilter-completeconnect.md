---
description: CTransformFilter. CompleteConnect 方法-CompleteConnect 方法會完成 pin 連接。
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: 'CTransformFilter. CompleteConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e708745231f320d143c55403a75178e78432a162c3c89fc2c5fe8fd62cdd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687308"
---
# <a name="ctransformfiltercompleteconnect-method"></a>CTransformFilter. CompleteConnect 方法

`CompleteConnect`方法會完成 pin 連接。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*direction* 
</dt> <dd>

[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定篩選上的哪個圖釘正在進行連接。

</dd> <dt>

*pReceivePin* 
</dt> <dd>

此連接嘗試中其他 pin 的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CTransformInputPin：： CompleteConnect**](ctransforminputpin-completeconnect.md)和 [**CTransformOutputPin：： CompleteConnect**](ctransformoutputpin-completeconnect.md)方法會在 pin 連接處理期間呼叫這個方法。 這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




