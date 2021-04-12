---
title: 'ICM_DRAW_START 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ 開始訊息會通知轉譯驅動程式，以在繪製框架的時機啟動其內部時鐘。 您可以使用 ICDrawStart 宏明確地傳送此訊息。
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384482"
---
# <a name="icm_draw_start-message"></a>ICM \_ 繪圖 \_ 開始訊息

**ICM \_ DRAW \_ 開始** 訊息會通知轉譯驅動程式，以在繪製框架的時機啟動其內部時鐘。 您可以使用 [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) 宏明確地傳送此訊息。


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

此訊息是由執行自己的非同步解壓縮、時間和繪圖的硬體所使用。

當驅動程式收到此訊息時，它應該會以 [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) 訊息指定的速率開始轉譯資料。

**Icm \_ 繪圖 \_ 開始** 和 [**ICM \_ 繪圖 \_ 停止**](icm-draw-stop.md)訊息不會被嵌套。 如果您的驅動程式會在使用 **icm \_ draw \_ STOP** 停止轉譯之前收到 **icm \_ draw \_ 開始**，則應該以新的參數重新開機轉譯。

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

 

 





