---
description: Put \_ system.windows.window.windowstate 方法會設定視窗狀態。
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: 'CBaseControlWindow.put_WindowState 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984757"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>CBaseControlWindow. put \_ system.windows.window.windowstate 方法

`put_WindowState`方法會設定視窗狀態。

## <a name="syntax"></a>語法


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*System.windows.window.windowstate* 
</dt> <dd>

新的視窗狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會採用與 Microsoft Win32 **ShowWindow** 函式相同的參數 (例如，ws \_ SHOWNORMAL、WS \_ SHOWMINNOACTI加值稅E 和 ws \_ SHOWMAXIMIZED) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




