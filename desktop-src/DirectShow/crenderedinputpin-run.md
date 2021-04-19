---
description: Run 方法會通知釘選篩選現在正在執行。 這個方法會覆寫 CBasePin：： Run 方法。
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: 'CRenderedInputPin： Run 方法 (Amextra) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987152"
---
# <a name="crenderedinputpinrun-method"></a>CRenderedInputPin 方法

`Run`方法會通知釘選篩選現在正在執行。 這個方法會覆寫 [**CBasePin：： Run**](cbasepin-run.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStart* 
</dt> <dd>

傳遞至篩選器 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 方法的開始時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amextra (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRenderedInputPin 類別**](crenderedinputpin.md)
</dt> </dl>

 

 




