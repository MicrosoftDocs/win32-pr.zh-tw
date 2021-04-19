---
description: 當視窗未最大化或最小化時，GetRestorePosition 方法會抓取要還原的位置。
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: 'CBaseControlWindow. GetRestorePosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995741"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>CBaseControlWindow. GetRestorePosition 方法

`GetRestorePosition`當視窗未最大化或最小化時，此方法會抓取要還原的位置。

## <a name="syntax"></a>語法


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pLeft* 
</dt> <dd>

最左邊座標值的指標。

</dd> <dt>

*pTop* 
</dt> <dd>

視窗頂端值的指標。

</dd> <dt>

*pWidth* 
</dt> <dd>

視窗寬度值的指標。

</dd> <dt>

*pHeight* 
</dt> <dd>

視窗高度值的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

當視窗未最大化或最小化時，這與 [**CBaseControlWindow：： GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) 函數所傳回的值相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




