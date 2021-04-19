---
description: CompleteConnect 方法會完成與另一個 pin 的連接。
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: 'CTransformOutputPin. CompleteConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d0c9c9fc7096191d7cdedffa21e2639fa0750ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995086"
---
# <a name="ctransformoutputpincompleteconnect-method"></a>CTransformOutputPin. CompleteConnect 方法

`CompleteConnect`方法會完成與另一個 pin 的連接。

## <a name="syntax"></a>語法


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pReceivePin* 
</dt> <dd>

指向其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseOutputPin：： CompleteConnect**](cbaseoutputpin-completeconnect.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： CompleteConnect**](ctransformfilter-completeconnect.md) 方法，它會 \_ 在基類中傳回 s OK。 衍生類別可以覆寫 **CTransformFilter：： CompleteConnect** 方法，以執行額外的檢查。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




