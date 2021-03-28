---
description: 當使用者在已將本身註冊為已卸載檔案收件者的應用程式視窗上放置檔案時傳送。
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: 'WM_DROPFILES 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973105"
---
# <a name="wm_dropfiles-message"></a>WM \_ DROPFILES 訊息

當使用者在已將本身註冊為已卸載檔案收件者的應用程式視窗上放置檔案時傳送。


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDrop* 
</dt> <dd>

描述已卸載檔案之內部結構的控制碼。 將此控制碼傳遞給 [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish)、 [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)或 [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) ，以取得已卸載檔案的相關資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

HDROP 控制碼是在 Shellapi 中宣告的。 您必須在組建中包含此標頭，才能使用 **WM \_ DROPFILES**。 如需如何使用拖放來傳送 Shell 資料的進一步討論，請參閱 [使用拖放或剪貼簿來傳送 Shell 資料](dragdrop.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**DragAcceptFiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
