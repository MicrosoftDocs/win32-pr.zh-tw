---
title: 'ICM_DRAW_START 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ 啟動訊息會通知轉譯驅動程式，以便在繪製框架的時機啟動其內部時鐘。 您可以使用 ICDrawStart 宏明確地傳送此訊息。
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START 訊息 Windows 多媒體
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
ms.openlocfilehash: 720d8c2f919d2b00955892a42ba8fca95b2b426c3cbb396aa4ac71a5cf912307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690948"
---
# <a name="icm_draw_start-message"></a>ICM \_繪製 \_ 開始訊息

**ICM \_ DRAW \_ 啟動** 訊息會通知轉譯驅動程式，以便在繪製框架的時機啟動其內部時鐘。 您可以使用 [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) 宏明確地傳送此訊息。


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

此訊息是由執行自己的非同步解壓縮、時間和繪圖的硬體所使用。

當驅動程式收到此訊息時，它應該會以 [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) message 指定的速率來開始轉譯資料。

**ICM \_ 繪製 \_ 啟動** 和 [**ICM \_ 繪製 \_ 停止**](icm-draw-stop.md)的訊息不會被嵌套。 如果您的驅動程式收到 ICM 繪製在使用 **ICM \_ 繪製 \_ 停止** 之前 **\_ \_ 開始** 轉譯，則應該重新開機以新參數呈現。

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

 

 





