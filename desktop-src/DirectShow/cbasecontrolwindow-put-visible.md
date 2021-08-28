---
description: Put \_ Visible 方法會顯示或隱藏視窗。
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: 'CBaseControlWindow.put_Visible 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2c8565d14c58d520a91c682e55d3dbc2ba079cf956213bdc61d044834d690c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793288"
---
# <a name="cbasecontrolwindowput_visible-method"></a>CBaseControlWindow。 put \_ Visible 方法

`put_Visible`方法會顯示或隱藏視窗。

## <a name="syntax"></a>語法


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Visible* 
</dt> <dd>

自動化布林值旗標 (0 表示視窗已隱藏，1表示視窗顯示) 。

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

 

 




