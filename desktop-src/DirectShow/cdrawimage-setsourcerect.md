---
description: SetSourceRect 方法會設定來源矩形。
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: 'CDrawImage. SetSourceRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990517"
---
# <a name="cdrawimagesetsourcerect-method"></a>CDrawImage. SetSourceRect 方法

`SetSourceRect`方法會設定來源矩形。

## <a name="syntax"></a>語法


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSourceRect* 
</dt> <dd>

**矩形** 結構的指標，此結構會定義新的來源矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果來源矩形變更，則擁有篩選應呼叫這個方法。例如，回應 [**IBasicVideo：： SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) 呼叫。

在呼叫這個方法之前，請先驗證 *pSourceRect* 中指定的矩形，以確定它不會延伸到原生影片大小之外。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




