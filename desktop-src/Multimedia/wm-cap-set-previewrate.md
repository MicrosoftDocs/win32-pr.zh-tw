---
title: 'WM_CAP_SET_PREVIEWRATE 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ PREVIEWRATE 訊息會以預覽模式設定畫面格顯示速率。 您可以使用 capPreviewRate 宏明確地傳送此訊息。
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935042"
---
# <a name="wm_cap_set_previewrate-message"></a>WM \_ CAP \_ 設定 \_ PREVIEWRATE 訊息

**WM \_ CAP \_ 設定 \_ PREVIEWRATE** 訊息會以預覽模式設定畫面格顯示速率。 您可以使用 [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*Wms*
</dt> <dd>

捕捉及顯示新框架的速率（以毫秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

預覽模式會使用大量的 CPU 資源。 當另一個應用程式具有焦點時，應用程式可以停用預覽或降低預覽率。 在串流處理影片捕獲期間，預覽工作的優先順序高於將畫面格寫入磁片的優先順序，而且只有在沒有其他緩衝區可供寫入時，才會顯示預覽畫面格。

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

 

 





