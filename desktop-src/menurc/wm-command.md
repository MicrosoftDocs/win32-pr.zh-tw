---
title: 'WM_COMMAND 訊息 (Winuser .h) '
description: 當使用者從功能表中選取命令專案時、控制項將通知訊息傳送至其父視窗，或翻譯快速鍵按鍵時傳送。
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001600"
---
# <a name="wm_command-message"></a>WM \_ 命令訊息

當使用者從功能表中選取命令專案時、控制項將通知訊息傳送至其父視窗，或翻譯快速鍵按鍵時傳送。


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

如需此參數的描述，請參閱備註。

</dd> <dt>

*lParam* 
</dt> <dd>

如需此參數的描述，請參閱備註。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="example"></a>範例

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples) 取得的範例。


## <a name="remarks"></a>備註

這裡摘要說明 *wParam* 和 *lParam* 參數的使用方式。



| 訊息來源 | wParam (high word)                 | wParam (低字組)                 | lParam                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| 功能表           | 0                                 |  (IDM) 的功能表識別碼 \_ \*        | 0                            |
| 加速器    | 1                                 |  (IDM) 的加速器識別碼 \_ \* | 0                            |
| 控制        | 控制項定義的通知碼 | 控制項識別碼               | 控制視窗的控制碼 |



 

### <a name="menus"></a>功能表

如果應用程式啟用功能表分隔符號，則當使用者選取分隔符號時，系統會傳送包含 *wParam* 參數低字的 **WM \_ 命令** 訊息（設為零）。

如果功能表定義了 [**MENUINFO 的 dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) 值，則會傳送 **\_** [**wm \_ MENUCOMMAND**](wm-menucommand.md) 而非 **wm \_ 命令**。

### <a name="accelerators"></a>快速鍵

從 [視窗] 功能表中選取專案的快速鍵按鍵會轉譯成 [**WM \_ SYSCOMMAND**](wm-syscommand.md) 訊息。

當擁有功能表的視窗最小化時，如果出現對應至功能表項目的快速鍵按鍵，則不會傳送任何 **WM \_ 命令** 訊息。 但是，如果出現的快速鍵不符合視窗功能表或 [視窗] 功能表中的任何專案，則會傳送 **WM \_ 命令** 訊息，即使視窗最小化也一樣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

