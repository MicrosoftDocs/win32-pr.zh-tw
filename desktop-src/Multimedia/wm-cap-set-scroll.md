---
title: 'WM_CAP_SET_SCROLL 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 捲軸訊息會定義要在 [捕捉] 視窗中顯示的影片畫面部分。
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466865"
---
# <a name="wm_cap_set_scroll-message"></a>WM \_ CAP \_ 設定 \_ 捲軸訊息

**WM \_ CAP \_ 設定 \_ 滾動** 條訊息會定義要在 [捕捉] 視窗中顯示的影片畫面部分。 這則訊息會將 [capture] 視窗工作區的左上角，設定為影片框架內指定圖元的座標。 您可以使用 [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*
</dt> <dd>

要包含所需滾動位置的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

捲軸位置會影響預覽和重迭模式中的影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[影片捕獲訊息](video-capture-messages.md)
</dt> </dl>

 

 





