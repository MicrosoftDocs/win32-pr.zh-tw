---
description: Put \_ width 方法會設定視窗寬度。
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: 'CBaseControlWindow.put_Width 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5235e2b842b26f3f05c31c9f19a16c7630c80c13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995507"
---
# <a name="cbasecontrolwindowput_width-method"></a>CBaseControlWindow。 put \_ Width 方法

`put_Width`方法會設定視窗寬度。

## <a name="syntax"></a>語法


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*寬度* 
</dt> <dd>

新視窗寬度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

視窗具有桌面上的位置。 這是以圖元為單位來表示， (左、上、右和下) 。 OLE 自動化的介面通常會以左、上、寬度和高度表示此位置;這是用於 DirectShow 的慣例。 所有座標都會以圖元表示，而變更任何座標都會立即更新視窗。

設定左方或上座標會將視窗分別向上或向下移動;這些座標不會影響視窗的寬度和高度。 同樣地，設定寬度和高度並不會影響左邊和上座標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




