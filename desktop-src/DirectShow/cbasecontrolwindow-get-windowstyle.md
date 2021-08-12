---
description: Get \_ system.windows.window.windowstyle 方法會抓取標準的視窗樣式。
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: 'CBaseControlWindow.get_WindowStyle 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9356b449adbb4ee760ec70990c4db0b6703c16e9d0970f2756bac23907b1bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660257"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a>CBaseControlWindow. 取得 \_ system.windows.window.windowstyle 方法

方法會抓取 `get_WindowStyle` 標準的視窗樣式。

## <a name="syntax"></a>語法


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWindowStyle* 
</dt> <dd>

視窗樣式的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會傳回標準視窗樣式，例如 WS \_ CHILD 和 ws \_ 。 它會呼叫 [**CBaseControlWindow：:D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) 成員函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




