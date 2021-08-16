---
title: 'WM_CAP_SET_PREVIEW 訊息 (Vfw .h) '
description: WM \_ CAP \_ 集 \_ 預覽訊息會啟用或停用預覽模式。
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25bf7f1ce2a61cb104c1e1764f9bca9c82d3aa40d44cc8a1eef9ce435584271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369382"
---
# <a name="wm_cap_set_preview-message"></a>WM \_ CAP \_ 設定 \_ 預覽訊息

**WM \_ CAP \_ 集 \_ 預覽** 訊息會啟用或停用預覽模式。 在 [預覽] 模式中，畫面格會從捕獲硬體傳輸到系統記憶體，然後使用 GDI 函數顯示在 [捕捉] 視窗中。 您可以使用 [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

預覽旗標。 針對此參數指定 **TRUE** 以啟用預覽模式，或指定 **FALSE** 來停用它。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

預覽模式會使用大量的 CPU 資源。 當另一個應用程式具有焦點時，應用程式可以停用預覽或降低預覽率。 [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構的 **fLiveWindow** 成員會指出目前是否已啟用預覽模式。

啟用預覽模式會自動停用覆迭模式。

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

 

 





