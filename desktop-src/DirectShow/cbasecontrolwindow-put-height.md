---
description: Put \_ height 方法會設定視窗高度。
ms.assetid: 11026ee5-e83a-4d82-9069-a302d55a2d46
title: 'CBaseControlWindow.put_Height 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798719c60b830caebee348032abce3e39a742e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999479"
---
# <a name="cbasecontrolwindowput_height-method"></a>CBaseControlWindow。 put \_ Height 方法

`put_Height`方法會設定視窗高度。

## <a name="syntax"></a>語法


```C++
HRESULT put_Height(
   long Height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*高度* 
</dt> <dd>

新視窗高度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

視窗具有桌面上的位置。 這是以圖元為單位來表示， (左、上、右和下) 。 OLE 自動化的介面通常會以左、上、寬度和高度表示此位置;這是用於 DirectShow 的慣例。 所有座標都會以圖元表示，而變更任何座標都會立即更新視窗。

設定左方或上座標會分別將視窗向左或上移動;這些座標不會影響視窗的寬度和高度。 同樣地，設定寬度和高度並不會影響左邊和上座標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




