---
title: 'WM_CAP_DLG_VIDEOCOMPRESSION 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION] 訊息會顯示一個對話方塊，讓使用者可以在此對話方塊中選取要在捕獲進程期間使用的壓縮程式。'
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025065"
---
# <a name="wm_cap_dlg_videocompression-message"></a>WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION 訊息

[ **WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION** ] 訊息會顯示一個對話方塊，讓使用者可以在此對話方塊中選取要在捕獲進程期間使用的壓縮程式。 可用的壓縮機清單會隨著 [捕捉驅動程式的影片格式] 對話方塊中選取的影片格式而有所不同。 您可以使用 [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) 宏明確地傳送此訊息。


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

使用此訊息搭配只提供 BI RGB 格式之框架的捕獲驅動程式 \_ 。 這則訊息最適合用於在單一作業中合併捕捉和壓縮的步驟捕獲作業。 使用軟體壓縮程式將框架壓縮為即時捕捉作業的一部分，很可能太耗時而無法執行。

壓縮不會影響複製到剪貼簿的畫面。

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

 

 





