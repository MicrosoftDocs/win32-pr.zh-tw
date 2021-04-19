---
description: 函式方法。
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: 'CDispParams. CDispParams (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989869"
---
# <a name="cdispparamscdispparams-constructor"></a>CDispParams. CDispParams 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nArgs* 
</dt> <dd>

傳遞給方法或屬性的引數數目。

</dd> <dt>

*pArgs* 
</dt> <dd>

引數清單的指標。 在清單中，每個引數都會儲存其 variant 類型。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDispParams 類別**](cdispparams.md)
</dt> </dl>

 

 




