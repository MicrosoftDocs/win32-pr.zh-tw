---
title: 'WM_CAP_SET_SCALE 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 規模訊息可啟用或停用預覽版影片影像的縮放比例。
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293be6917917581957df0f5dae9456274f1d2cc3eeffff5ea971c3596209a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369392"
---
# <a name="wm_cap_set_scale-message"></a>WM \_ CAP \_ 設定 \_ 調整訊息

**WM \_ CAP \_ 設定 \_ 規模** 訊息可啟用或停用預覽版影片影像的縮放比例。 如果已啟用縮放，則會將已捕捉的影片畫面延展至 [捕獲] 視窗的維度。 您可以使用 [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

預覽調整旗標。 針對此參數指定 **TRUE** ，以將預覽框架延展至 [捕獲] 視窗的大小，或為 **FALSE** 以其自然大小顯示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

調整預覽影像會控制捕捉視窗內所捕獲框架的立即呈現。 它不會影響儲存至檔案的框架大小。

使用重迭來顯示框架緩衝區中的影片時，縮放比例沒有任何作用。

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

 

 





