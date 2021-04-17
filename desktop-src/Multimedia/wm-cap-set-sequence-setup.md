---
title: 'WM_CAP_SET_SEQUENCE_SETUP 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 順序 \_ 安裝程式訊息會設定用於串流處理捕獲的設定參數。 您可以使用 capCaptureSetSetup 宏明確地傳送此訊息。
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509359"
---
# <a name="wm_cap_set_sequence_setup-message"></a>WM \_ CAP \_ 設定 \_ 順序設定 \_ 訊息

**WM \_ CAP \_ 設定 \_ 順序 \_ 安裝程式** 訊息會設定用於串流處理捕獲的設定參數。 您可以使用 [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**S** 所參考之結構的大小（以位元組為單位）。

</dd> <dt>

<span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*
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

 

 





