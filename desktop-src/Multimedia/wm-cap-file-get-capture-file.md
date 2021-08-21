---
title: 'WM_CAP_FILE_GET_CAPTURE_FILE 訊息 (Vfw .h) '
description: WM \_ CAP 檔案 \_ 取得捕獲檔案訊息會傳回 \_ 目前 CAPTURE 檔案的 \_ \_ 名稱。 您可以使用 capFileGetCaptureFile 宏明確地傳送此訊息。
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462f919458078129f6756782c2fde5322b3cd814c3108cb0ba8ee24e2f54c022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135316"
---
# <a name="wm_cap_file_get_capture_file-message"></a>WM \_ CAP \_ 檔案 \_ 取得 \_ 捕獲檔案 \_ 訊息

**WM \_ CAP 檔案 \_ \_ 取得 \_ 捕獲 \_** 檔案訊息會傳回目前 CAPTURE 檔案的名稱。 您可以使用 [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) 宏明確地傳送此訊息。


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**>Szname** 所參考的應用程式定義緩衝區大小（以位元組為單位）。

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*
</dt> <dd>

應用程式定義的緩衝區指標，用來將捕獲檔案的名稱當做以 null 終止的字串傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

預設的捕獲檔案名為 C： \\CAPTURE.AVI。

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

 

 





