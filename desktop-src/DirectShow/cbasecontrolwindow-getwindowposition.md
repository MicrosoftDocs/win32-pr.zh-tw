---
description: GetWindowPosition 方法會抓取視窗目前的座標。
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: 'CBaseControlWindow. GetWindowPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d576f065e807c2af47621d43940d7e48c54f36f0617d20590953a5e83ab2fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966728"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>CBaseControlWindow. GetWindowPosition 方法

方法會抓取 `GetWindowPosition` 視窗目前的座標。

## <a name="syntax"></a>語法


```C++
HRESULT GetWindowPosition(
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

左邊座標的指標，以螢幕座標為單位。

</dd> <dt>

*pTop* 
</dt> <dd>

頂端座標的指標，以螢幕座標為單位。

</dd> <dt>

*pWidth* 
</dt> <dd>

視窗寬度的指標，以螢幕座標為單位。

</dd> <dt>

*pHeight* 
</dt> <dd>

視窗高度的指標（以螢幕座標表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




