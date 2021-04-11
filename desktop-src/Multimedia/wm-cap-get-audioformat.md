---
title: 'WM_CAP_GET_AUDIOFORMAT 訊息 (Vfw .h) '
description: WM \_ CAP \_ GET \_ AUDIOFORMAT 訊息會取得音訊格式或音訊格式的大小。 您可以使用 capGetAudioFormat 和 capGetAudioFormatSize 宏明確地傳送此訊息。
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383846"
---
# <a name="wm_cap_get_audioformat-message"></a>WM \_ CAP \_ 取得 \_ AUDIOFORMAT 訊息

**WM \_ CAP \_ GET \_ AUDIOFORMAT** 訊息會取得音訊格式或音訊格式的大小。 您可以使用 [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) 和 [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) 宏明確地傳送此訊息。


```C++
WM_CAP_GET_AUDIOFORMAT 
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

[**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構的指標，或 **為 Null**。 如果值為 **Null**，則會傳回保存結構所需的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回音頻格式的大小（以位元組為單位）。

## <a name="remarks"></a>備註

由於壓縮的音訊格式因大小需求而異，因此應用程式必須先取出大小，然後配置記憶體，最後要求音訊格式資料。

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

 

