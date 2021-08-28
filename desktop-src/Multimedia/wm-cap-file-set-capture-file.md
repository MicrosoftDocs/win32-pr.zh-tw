---
title: 'WM_CAP_FILE_SET_CAPTURE_FILE 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ file \_ SET \_ CAPTURE \_ file] 訊息會將用於影片捕獲的檔案命名為。 您可以使用 capFileSetCaptureFile 宏明確地傳送此訊息。'
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9435a7f0790c8ffe88f6b7ea6228bb2f442b23f5dcb15e2722e59b75c671588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687018"
---
# <a name="wm_cap_file_set_capture_file-message"></a>WM \_ CAP \_ file \_ SET \_ CAPTURE \_ file 訊息

[ **WM \_ CAP \_ file \_ SET \_ CAPTURE \_ file** ] 訊息會將用於影片捕獲的檔案命名為。 您可以使用 [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) 宏明確地傳送此訊息。


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*
</dt> <dd>

以 null 結束的字串指標，其中包含要使用的捕獲檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果檔案名無效，或如果正在進行資料流程或單一框架捕獲，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息會將檔案名儲存在內部結構中。 它不會建立、配置或開啟指定的檔案。 預設的捕獲檔案名為 C： \\CAPTURE.AVI。

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

 

 





