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
ms.openlocfilehash: 6d8dbdc67bfec4e2f649992520d5dd79e4a396f76e5c8d17df81da1bead07cd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908448"
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

 

 




