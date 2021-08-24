---
description: Put \_ top 方法會設定頂端視窗座標。
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: 'CBaseControlWindow.put_Top 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3332bcf90ac5e2ee776fe7110c958e50b838bcbdbc6bb4abb23850ced12cc28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635828"
---
# <a name="cbasecontrolwindowput_top-method"></a>CBaseControlWindow。 put \_ Top 方法

`put_Top`方法會設定頂端視窗座標。

## <a name="syntax"></a>語法


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*前幾個* 
</dt> <dd>

新的最大座標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

視窗具有桌面上的位置。 這是以圖元為單位來表示， (左、上、右和下) 。 OLE 自動化的介面通常會以左、上、寬度和高度表示此位置;這是 DirectShow 中使用的慣例。 所有座標都會以圖元表示，而變更任何座標都會立即更新視窗。

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

 

 




