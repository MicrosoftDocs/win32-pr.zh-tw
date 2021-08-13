---
description: Get \_ left 方法會抓取目前的左視窗座標。
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: 'CBaseControlWindow.get_Left 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9317c1c061fe8528903bdd2e7129d0cfdc9e6dd67b9722841360d131e15cfb10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660521"
---
# <a name="cbasecontrolwindowget_left-method"></a>CBaseControlWindow。取得 \_ 左方方法

方法會抓取 `get_Left` 目前的左視窗座標。

## <a name="syntax"></a>語法


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pLeft* 
</dt> <dd>

左邊座標的指標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

視窗具有桌面上的位置。 這個位置是以圖元為單位來表示， (左、上、右和下) 。 OLE 自動化的介面通常會以左、上、寬度和高度表示此位置;這是 DirectShow 中使用的慣例。 所有座標都會以圖元表示，而變更任何座標都會立即更新視窗。

設定左方或上座標會分別將視窗向左和向上移動;這些座標不會影響視窗的寬度和高度。 同樣地，設定寬度和高度不會影響左邊和上座標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




