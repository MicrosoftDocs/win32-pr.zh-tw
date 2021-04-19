---
description: ScheduleSample 方法會覆寫執行主要工作的基類，以保留 IQualProp 實) 所使用 (所繪製樣本的計數。
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: 'CBaseVideoRenderer. ScheduleSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995628"
---
# <a name="cbasevideorendererschedulesample-method"></a>CBaseVideoRenderer. ScheduleSample 方法

`ScheduleSample`方法會覆寫執行主要工作的基類，以保留 [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop)實) 所使用 (所繪製樣本的計數。

## <a name="syntax"></a>語法


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

媒體範例的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已排程範例，則傳回 **TRUE** ;否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




