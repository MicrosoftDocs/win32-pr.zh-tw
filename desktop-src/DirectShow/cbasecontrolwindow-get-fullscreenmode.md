---
description: Get \_ FullScreenMode 方法會抓取目前的全螢幕模式。
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: 'CBaseControlWindow.get_FullScreenMode 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978776"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a>CBaseControlWindow. 取得 \_ FullScreenMode 方法

方法會抓取 `get_FullScreenMode` 目前的全螢幕模式。

## <a name="syntax"></a>語法


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

目前全螢幕模式的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

依預設，此成員函式會傳回 E \_ >notimpl。 這會通知 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 外掛程式散發者，此轉譯器不會執行全螢幕轉譯器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




