---
title: 'WM_CAP_GET_SEQUENCE_SETUP 訊息 (Vfw .h) '
description: WM \_ CAP \_ GET \_ SEQUENCE 設定訊息會抓取 \_ 串流處理捕獲參數的目前設定。 您可以使用 capCaptureGetSetup 宏明確地傳送此訊息。
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55122a98846f23c609eb371ab5698198729c39e967d7953295850b61764459af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369536"
---
# <a name="wm_cap_get_sequence_setup-message"></a>WM \_ CAP \_ 取得 \_ 順序 \_ 設定訊息

**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定** 訊息會抓取串流處理捕獲參數的目前設定。 您可以使用 [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏明確地傳送此訊息。


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**S** 所參考之結構的大小（以位元組為單位）。

</dd> <dt>

<span id="s"></span><span id="S"></span>*！*
</dt> <dd>

[**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如需用來控制串流處理捕獲之參數的相關資訊，請參閱 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構。

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

 

 





