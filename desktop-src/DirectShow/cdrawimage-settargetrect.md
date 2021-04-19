---
description: SetTargetRect 方法會設定目標矩形。
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: 'CDrawImage. SetTargetRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000774"
---
# <a name="cdrawimagesettargetrect-method"></a>CDrawImage. SetTargetRect 方法

`SetTargetRect`方法會設定目標矩形。

## <a name="syntax"></a>語法


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTargetRect* 
</dt> <dd>

**矩形** 結構的指標，此結構會定義新的目標矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果來源矩形變更，則擁有篩選應呼叫這個方法。例如，回應 [**IBasicVideo：： SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) 呼叫。

在呼叫這個方法之前，請先驗證 *pTargetRect*（相對於影片視窗）中所指定的矩形。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




