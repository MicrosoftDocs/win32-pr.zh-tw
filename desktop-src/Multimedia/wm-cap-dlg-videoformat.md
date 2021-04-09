---
title: 'WM_CAP_DLG_VIDEOFORMAT 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ DLG \_ VIDEOFORMAT] 訊息會顯示一個對話方塊，讓使用者可以在其中選取影片格式。'
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934251"
---
# <a name="wm_cap_dlg_videoformat-message"></a>WM \_ CAP \_ DLG \_ VIDEOFORMAT 訊息

[ **WM \_ CAP \_ DLG \_ VIDEOFORMAT** ] 訊息會顯示一個對話方塊，讓使用者可以在其中選取影片格式。 您可以使用 [影片格式] 對話方塊來選取影像尺寸、位深度和硬體壓縮選項。 您可以使用 [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) 宏明確地傳送此訊息。


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息傳回之後，應用程式可能需要更新 [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) 結構，因為使用者可能已變更影像維度。

每個 capture 驅動程式的 [影片格式] 對話方塊都是唯一的。 某些捕獲驅動程式可能不支援 [影片格式] 對話方塊。 應用程式可以藉由檢查 [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)的 **fHasDlgVideoFormat** 成員，判斷 capture 驅動程式是否支援此訊息。

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

 

 





