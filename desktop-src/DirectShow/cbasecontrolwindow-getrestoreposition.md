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
ms.openlocfilehash: 215b71d731227641df02716dd2b760f7e023bbec0c50bc66ac6d390ed87d002e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757608"
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

 

 




