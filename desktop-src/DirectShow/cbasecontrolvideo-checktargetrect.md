---
description: CheckTargetRect 方法會判斷目標矩形是否有效。
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: 'CBaseControlVideo. CheckTargetRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8444764af729f9536471a6a9df221cc118edb7d043112eb0b5351f45982d87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057318"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>CBaseControlVideo. CheckTargetRect 方法

`CheckTargetRect`方法會判斷目標矩形是否有效。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTargetRect* 
</dt> <dd>

要檢查的目標矩形指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果無效 \_ ，則傳回 E INVALIDARG，否則會傳回 >aad-userreadusingalternativesecurityid-noerror (S \_ OK) 。

## <a name="remarks"></a>備註

此成員函式會判斷所要求的目標矩形是否有效。 因為目的矩形會在視窗的邏輯用戶端中指定位置，所以座標可以是負數，但整體寬度和高度不能是零或負數值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




