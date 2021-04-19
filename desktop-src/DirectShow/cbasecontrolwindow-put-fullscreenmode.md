---
description: Put \_ FullScreenMode 方法會設定轉譯器的全螢幕模式。
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: 'CBaseControlWindow.put_FullScreenMode 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999356"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>CBaseControlWindow. put \_ FullScreenMode 方法

方法會設定轉譯器 `put_FullScreenMode` 的全螢幕模式。

## <a name="syntax"></a>語法


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

要套用的全螢幕模式。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 目前的執行會傳回 E \_ >notimpl。

## <a name="remarks"></a>備註

執行全螢幕模式的影片轉譯器應該覆寫這個成員函式，並執行它所支援的任何模式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




