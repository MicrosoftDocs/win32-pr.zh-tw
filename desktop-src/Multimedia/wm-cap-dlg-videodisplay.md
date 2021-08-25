---
title: 'WM_CAP_DLG_VIDEODISPLAY 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ DLG \_ VIDEODISPLAY] 訊息會顯示一個對話方塊，讓使用者可以在其中設定或調整影片輸出。'
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16afffbf1d3450670b99d26303627771aa4bd3399a252cd16a68bc690012f541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803868"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>WM \_ CAP \_ DLG \_ VIDEODISPLAY 訊息

[ **WM \_ CAP \_ DLG \_ VIDEODISPLAY** ] 訊息會顯示一個對話方塊，讓使用者可以在其中設定或調整影片輸出。 此對話方塊可能包含影響所顯示影像的色調、對比和亮度，以及按鍵色彩對齊的控制項。 您可以使用 [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) 宏明確地傳送此訊息。


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此對話方塊中的控制項不會影響數位化的影片資料。它們只會影響視訊訊號的輸出或重新顯示。

[影片顯示] 對話方塊對每個 capture 驅動程式而言都是唯一的。 某些捕獲驅動程式可能不支援 [影片顯示] 對話方塊。 應用程式可以藉由檢查 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)結構的 **fHasDlgVideoDisplay** 成員，判斷 capture 驅動程式是否支援此訊息。

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

 

 





