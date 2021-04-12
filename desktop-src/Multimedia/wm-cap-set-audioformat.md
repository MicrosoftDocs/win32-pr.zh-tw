---
title: 'WM_CAP_SET_AUDIOFORMAT 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ AUDIOFORMAT 訊息會設定執行串流或步驟捕捉時使用的音訊格式。 您可以使用 capSetAudioFormat 宏明確地傳送此訊息。
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- WM_CAP_SET_AUDIOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104153"
---
# <a name="wm_cap_set_audioformat-message"></a>WM \_ CAP \_ 設定 \_ AUDIOFORMAT 訊息

**WM \_ CAP \_ 設定 \_ AUDIOFORMAT** 訊息會設定執行串流或步驟捕捉時使用的音訊格式。 您可以使用 [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**S** 所參考之結構的大小（以位元組為單位）。

</dd> <dt>

<span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*
</dt> <dd>

定義音訊格式的 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) 或 [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

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

 

