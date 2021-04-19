---
title: 'WM_CAP_SET_CALLBACK_FRAME 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 回呼 \_ 框架訊息會在應用程式中設定預覽回撥函式。 當捕捉視窗捕獲預覽畫面時，AVICap 會呼叫這個程式。 您可以使用 capSetCallbackOnFrame 宏明確地傳送此訊息。
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966320"
---
# <a name="wm_cap_set_callback_frame-message"></a>WM \_ CAP \_ 設定 \_ 回呼 \_ 框架訊息

**WM \_ CAP \_ 設定 \_ 回呼 \_ 框架** 訊息會在應用程式中設定預覽回撥函式。 當捕捉視窗捕獲預覽畫面時，AVICap 會呼叫這個程式。 您可以使用 [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

預覽回呼函式的指標，其類型為 [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)。 針對此參數指定 **Null** ，以停用先前安裝的回呼函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

捕捉視窗會先呼叫回呼函式，再顯示預覽框架。 這可讓應用程式視需要修改框架。 串流處理影片捕獲期間未使用此回呼函數。

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

 

 





