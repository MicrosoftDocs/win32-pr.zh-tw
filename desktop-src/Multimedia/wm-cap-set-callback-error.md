---
title: 'WM_CAP_SET_CALLBACK_ERROR 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤訊息會在用戶端應用程式中設定錯誤回呼函數。 當發生錯誤時，AVICap 會呼叫這個程式。 您可以使用 capSetCallbackOnError 宏明確地傳送此訊息。
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465661"
---
# <a name="wm_cap_set_callback_error-message"></a>WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤訊息

**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤** 訊息會在用戶端應用程式中設定錯誤回呼函數。 當發生錯誤時，AVICap 會呼叫這個程式。 您可以使用 [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

錯誤回呼函數的指標，其類型為 [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)。 針對此參數指定 **Null** ，以停用先前安裝的錯誤回呼函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

應用程式可以選擇性地設定錯誤回呼函數。 如果設定，AVICap 會在下列情況下呼叫錯誤程式：

-   磁碟已滿。
-   無法使用 capture 驅動程式連接捕獲視窗。
-   無法開啟波形音訊裝置。
-   在 capture 期間卸載的框架數目超過指定的百分比。
-   由於有垂直的同步處理中斷問題，因此無法捕獲框架。

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

 

 





