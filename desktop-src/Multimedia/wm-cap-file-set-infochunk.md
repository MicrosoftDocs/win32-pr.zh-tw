---
title: 'WM_CAP_FILE_SET_INFOCHUNK 訊息 (Vfw .h) '
description: WM \_ CAP 檔案 \_ \_ 集 INFOCHUNK 訊息會設定 \_ 並清除資訊區塊。
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d64f88a87af63e5afc513e0e2cf2df53d64570bec099a2f8f2846d781fc0b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892068"
---
# <a name="wm_cap_file_set_infochunk-message"></a>WM \_ CAP \_ FILE \_ SET \_ INFOCHUNK message

**WM \_ CAP 檔案 \_ \_ 集 \_ INFOCHUNK** 訊息會設定並清除資訊區塊。 資訊區塊可以在 capture 期間插入 AVI 檔案中，以內嵌文字字串或自訂資料。 您可以使用 [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) 宏明確地傳送此訊息。


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*
</dt> <dd>

[**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk)結構的指標，定義要建立或刪除的資訊區塊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。

## <a name="remarks"></a>備註

您可以將多個已註冊的資訊區塊加入至 AVI 檔案。 設定資訊區塊之後，它會繼續新增至後續的捕獲檔案，直到清除專案或清除所有資訊區塊專案為止。 若要清除單一專案，請在 **fccInfoID** 成員中指定資訊區塊，並在 [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk)結構的 **lpData** 成員中指定 **Null** 。 若要清除所有專案，請在 **fccInfoID** 中指定 **Null** 。

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

 

 





