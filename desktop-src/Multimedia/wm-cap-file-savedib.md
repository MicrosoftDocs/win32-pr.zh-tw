---
title: 'WM_CAP_FILE_SAVEDIB 訊息 (Vfw .h) '
description: WM \_ CAP \_ file \_ SAVEDIB 訊息會將目前的畫面格複製到 DIB 檔案。 您可以使用 capFileSaveDIB 宏明確地傳送此訊息。
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66d6dd9b8675e1fb8625349afc4b3f86347d71d605407d5c99fbca291ade744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803808"
---
# <a name="wm_cap_file_savedib-message"></a>WM \_ CAP \_ FILE \_ SAVEDIB 訊息

**WM \_ CAP \_ file \_ SAVEDIB** 訊息會將目前的畫面格複製到 DIB 檔案。 您可以使用 [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) 宏明確地傳送此訊息。


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*
</dt> <dd>

以 null 結束的字串指標，其中包含目的地 DIB 檔案的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。

## <a name="remarks"></a>備註

如果捕捉驅動程式提供壓縮格式的框架，此呼叫會先嘗試解壓縮框架再寫入檔案。

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

 

 





