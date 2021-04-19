---
description: DoGetWindowStyle 方法會抓取目前的一般或擴充的視窗樣式。
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: 'CBaseControlWindow. DoGetWindowStyle 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976076"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>CBaseControlWindow. DoGetWindowStyle 方法

方法會抓取 `DoGetWindowStyle` 目前的一般或擴充的視窗樣式。

## <a name="syntax"></a>語法


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStyle* 
</dt> <dd>

接收樣式資訊之變數的指標。

</dd> <dt>

*WindowLong* 
</dt> <dd>

值，指定要取出的樣式。 必須是下列其中之一：



|              |                                      |
|--------------|--------------------------------------|
| GWL \_ 樣式   | 取出視窗樣式。          |
| GWL \_ EXSTYLE | 取出擴充的視窗樣式。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會呼叫 Win32 **GetWindowLong** 函式，以取得視窗樣式。 它是由 [**CBaseControlWindow：： get \_ System.windows.window.windowstyle**](cbasecontrolwindow-get-windowstyle.md) 和 [**CBaseControlWindow：： get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) 成員函式所呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




