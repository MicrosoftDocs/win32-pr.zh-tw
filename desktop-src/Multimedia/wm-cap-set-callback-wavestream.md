---
title: 'WM_CAP_SET_CALLBACK_WAVESTREAM 訊息 (Vfw .h) '
description: WM \_ CAP \_ SET \_ 回呼 \_ WAVESTREAM 訊息會在應用程式中設定回呼函數。
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e4a8ef585a3ceb35aa07fe4e31c5819ce3e56d20b0bfd2d6c5f588fc25c335b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622517"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>WM \_ CAP \_ 設定 \_ 回呼 \_ WAVESTREAM 訊息

**WM \_ CAP \_ SET \_ 回呼 \_ WAVESTREAM** 訊息會在應用程式中設定回呼函數。 當新的音訊緩衝區可供使用時，AVICap 會在串流處理期間呼叫此程式。 您可以使用 [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Wave 資料流程回呼函數的指標，其類型為 [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)。 針對此參數指定 **Null** ，以停用先前安裝的 wave stream 回呼函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

「捕獲視窗」會在將音訊緩衝區寫入磁片之前呼叫程式。 這可讓應用程式視需要修改音訊緩衝區。

如果使用 wave 資料流程回呼函式，則必須先安裝該函式，才能啟動 capture 會話，且必須在會話持續時間內保持啟用狀態。 您可以在串流處理的結束之後停用此功能。

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

 

 





