---
description: SetWindowPosition 方法會設定桌面上的視窗位置。
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: 'CBaseControlWindow. SetWindowPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995360"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>CBaseControlWindow. SetWindowPosition 方法

`SetWindowPosition`方法會在桌面上設定視窗的位置。

## <a name="syntax"></a>語法


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*離開* 
</dt> <dd>

新的左座標。

</dd> <dt>

*前幾個* 
</dt> <dd>

新的上方座標。

</dd> <dt>

*寬度* 
</dt> <dd>

視窗的寬度。

</dd> <dt>

*高度* 
</dt> <dd>

視窗的高度。

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

 

 




