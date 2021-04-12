---
title: 'WM_CAP_FILE_ALLOCATE 訊息 (Vfw .h) '
description: WM \_ CAP 檔案 \_ \_ 配置訊息會建立 (會預先配置) 指定大小的捕捉檔。 您可以使用 capFileAlloc 宏明確地傳送此訊息。
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464733"
---
# <a name="wm_cap_file_allocate-message"></a>WM \_ CAP \_ FILE \_ 配置訊息

**WM \_ CAP 檔案 \_ \_ 配置** 訊息會建立 (會預先配置) 指定大小的捕捉檔。 您可以使用 [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) 宏明確地傳送此訊息。


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*
</dt> <dd>

建立 capture 檔案的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。

## <a name="remarks"></a>備註

您可以藉由預先配置夠大的捕獲檔案來儲存整個影片剪輯，以及在捕獲剪輯之前重組 capture 檔案，以大幅改善串流捕獲效能。

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

 

 





