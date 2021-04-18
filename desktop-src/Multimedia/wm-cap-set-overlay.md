---
title: 'WM_CAP_SET_OVERLAY 訊息 (Vfw .h) '
description: WM \_ CAP 集合重迭 \_ 訊息會 \_ 啟用或停用覆迭模式。 在重迭模式中，會使用硬體重迭來顯示影片。 您可以使用 capOverlay 宏明確地傳送此訊息。
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965326"
---
# <a name="wm_cap_set_overlay-message"></a>WM \_ CAP \_ 設定重迭 \_ 訊息

**WM \_ CAP \_ 集合 \_** 重迭訊息會啟用或停用覆迭模式。 在重迭模式中，會使用硬體重迭來顯示影片。 您可以使用 [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

覆迭旗標。 請為此參數指定 **TRUE** ，以啟用覆迭模式或 **FALSE** 來停用它。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

使用覆迭不需要 CPU 資源。

[**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)結構的 **fHasOverlay** 成員會指出裝置是否能夠進行重迭。 [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構的 **fOverlayWindow** 成員會指出目前是否已啟用覆迭模式。

啟用覆迭模式會自動停用預覽模式。

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

 

 





