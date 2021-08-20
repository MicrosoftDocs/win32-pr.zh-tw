---
description: GetMaxIdealImageSize 方法會抓取理想的影像大小上限。
ms.assetid: 881c1c3d-7505-44a2-964d-3255e2072f6b
title: 'CBaseControlWindow. GetMaxIdealImageSize 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMaxIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff87648e8f3866eaa4869f45dd0467cde614eb6b2d1405006b3df89966d8c8c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001033"
---
# <a name="cbasecontrolwindowgetmaxidealimagesize-method"></a>CBaseControlWindow. GetMaxIdealImageSize 方法

方法會抓取 `GetMaxIdealImageSize` 理想的影像大小上限。

## <a name="syntax"></a>語法


```C++
HRESULT GetMaxIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWidth* 
</dt> <dd>

最大理想寬度的指標（以圖元為單位）。

</dd> <dt>

*pHeight* 
</dt> <dd>

最大理想高度（以圖元為單位）的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

各種轉譯器對於可顯示的影像大小都有其效能限制。 雖然當要求顯示的影像大於指定的最大值時，仍可正常運作，但轉譯器可以透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面提名最小和最大的理想大小。 只有在篩選圖形暫停或正在執行時，才可以呼叫這個介面，因為它不會等到配置資源，而且轉譯器可以辨識其限制。 如果沒有任何限制，轉譯器會以原生影片維度填入 *pWidth* 和 *pHeight* 參數，並傳回 \_ FALSE。 如果有限制，則會輸入限制的寬度和高度，而且成員函式會傳回 S \_ OK。

這些維度會套用至目的地影片的大小，而不會套用到整體視窗大小。 因此，在計算要設定之視窗的大小時，請考慮目前的視窗樣式 (例如，WS \_ 標題和 ws \_ 框線) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




