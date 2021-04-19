---
description: CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。 這個方法會覆寫 CBasePin：： CheckMediaType 方法。
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: 'CRendererInputPin. CheckMediaType 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989624"
---
# <a name="crendererinputpincheckmediatype-method"></a>CRendererInputPin. CheckMediaType 方法

`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。 這個方法會覆寫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

媒體類型物件的指標，該物件包含建議的媒體類型。

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

 

 




