---
title: 'ICM_DRAW_END 訊息 (Vfw .h) '
description: ICM \_ 繪製 \_ 結束訊息會通知轉譯驅動程式將目前的影像解壓縮至螢幕，以及釋放配置給解壓縮和繪製的資源。 您可以使用 ICDrawEnd 宏明確地傳送此訊息。
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daac4fed37908596bab68b37bf5ae20c9c4652a6550288d52b892e640be612cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987442"
---
# <a name="icm_draw_end-message"></a>ICM \_繪製 \_ 結束訊息

**ICM \_ 繪製 \_ 結束** 訊息會通知轉譯驅動程式將目前的影像解壓縮至螢幕，以及釋放配置給解壓縮和繪製的資源。 您可以使用 [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) 宏明確地傳送此訊息。


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

[**ICM \_ draw \_ BEGIN**](icm-draw-begin.md)和 **ICM \_ draw \_ END** 訊息不會被嵌套。 如果您的驅動程式收到 **ICM \_ draw \_ 開始**，然後再以 **ICM \_ DRAW \_ END** 停止解壓縮，則應該以新的參數重新開機解壓縮。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 





