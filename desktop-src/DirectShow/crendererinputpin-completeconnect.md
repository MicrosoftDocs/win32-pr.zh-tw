---
description: CompleteConnect 方法會完成輸出釘選的連接。 這個方法會覆寫 CBasePin：： CompleteConnect 方法。
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: 'CRendererInputPin. CompleteConnect 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996087"
---
# <a name="crendererinputpincompleteconnect-method"></a>CRendererInputPin. CompleteConnect 方法

`CompleteConnect`方法會完成輸出釘選的連接。 這個方法會覆寫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 方法。

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

輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRendererInputPin 類別**](crendererinputpin.md)
</dt> </dl>

 

 




