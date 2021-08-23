---
title: 'WM_CAP_DLG_VIDEOSOURCE 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ DLG \_ VIDEOSOURCE] 訊息會顯示一個對話方塊，讓使用者可以在此對話方塊中控制影片來源。'
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f05d7e3dc421759229adffa4ecc4b78affc26f1b4244887b017614c2ab4d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803878"
---
# <a name="wm_cap_dlg_videosource-message"></a>WM \_ CAP \_ DLG \_ VIDEOSOURCE 訊息

[ **WM \_ CAP \_ DLG \_ VIDEOSOURCE** ] 訊息會顯示一個對話方塊，讓使用者可以在此對話方塊中控制影片來源。 [影片來源] 對話方塊可能包含選取輸入來源的控制項;改變影像的色調、對比、亮度;並在將影像數位化至框架緩衝區之前修改影片品質。 您可以使用 [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) 宏明確地傳送此訊息。


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

[影片來源] 對話方塊對每個 capture 驅動程式而言都是唯一的。 某些捕獲驅動程式可能不支援 [影片來源] 對話方塊。 應用程式可以藉由檢查 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)結構的 **fHasDlgVideoSource** 成員，判斷 capture 驅動程式是否支援此訊息。

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

 

 





