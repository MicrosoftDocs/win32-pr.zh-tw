---
description: IsAutoShowEnabled 方法會抓取當轉譯篩選暫停或執行時，是否會自動顯示影片視窗的相關資訊。
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: 'CBaseControlWindow. IsAutoShowEnabled 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990261"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>CBaseControlWindow. IsAutoShowEnabled 方法

`IsAutoShowEnabled`方法會抓取當轉譯篩選暫停或執行時，是否會自動顯示影片視窗的相關資訊。

## <a name="syntax"></a>語法


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果 **m \_ bAutoShow** 成員設為1，則傳回 **TRUE** ，如果設定為0，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果在隱藏的影片視窗上， **m \_ bAutoShow** 成員設為1，當篩選暫停或執行時，視窗就會變成可見。 如果這個成員設定為0，則只有在您使用 [**CBaseControlWindow：:p ui \_ Visible**](cbasecontrolwindow-put-visible.md) 或 [**CBaseControlWindow：:p 的 \_ system.windows.window.windowstate**](cbasecontrolwindow-put-windowstate.md) 成員函式搭配適當的參數時，才會出現此視窗。

此成員函式會抓取 **m \_ bAutoShow** 成員設定，並具有與使用 [**IVideoWindow：： get 自動完成 \_**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) 方法相同的結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




