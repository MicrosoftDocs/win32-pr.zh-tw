---
title: 'WM_CAP_GET_STATUS 訊息 (Vfw .h) '
description: WM \_ CAP \_ 取得 \_ 狀態訊息會抓取捕捉視窗的狀態。 您可以使用 capGetStatus 宏明確地傳送此訊息。
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024558"
---
# <a name="wm_cap_get_status-message"></a>WM \_ CAP \_ 取得 \_ 狀態訊息

**WM \_ CAP \_ 取得 \_ 狀態** 消息會抓取捕捉視窗的狀態。 您可以使用 [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) 宏明確地傳送此訊息。


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**S** 所參考之結構的大小（以位元組為單位）。

</dd> <dt>

<span id="s"></span><span id="S"></span>*！*
</dt> <dd>

[**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

[**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)結構包含 [capture] 視窗的目前狀態。 由於這個狀態是動態的，且因回應各種訊息而變更，因此應用程式應該在傳送 [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) 訊息之後初始化此結構 (或使用 [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) 宏) ，以及每次需要啟用功能表項目或判斷視窗的實際狀態。

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

 

 





