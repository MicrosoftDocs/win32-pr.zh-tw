---
title: 'WM_TOUCH 訊息 (Winuser .h) '
description: 當一或多個觸控點（例如手指或畫筆）觸及觸控式的數位化板介面時，通知視窗。
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH 訊息 Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1034a229dbb1f3895726fcb3c1551e2dd0f390be0fd7bc2eb81d8331e582eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810098"
---
# <a name="wm_touch-message"></a>WM \_ 觸控訊息

當一或多個觸控點（例如手指或畫筆）觸及觸控式的數位化板介面時，通知視窗。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位文字包含與此訊息相關聯的觸控點數目。 高序位字組保留供日後使用。

</dd> <dt>

*lParam* 
</dt> <dd>

包含觸控輸入控點，可用於 [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) 的呼叫，以取得與此訊息相關聯之觸控點的詳細資訊。

這個控制碼只在目前的進程內有效，不應該跨進程傳遞，除非 **LPARAM** 在 **SendMessage** 或 **PostMessage** 呼叫中。

當應用程式不再需要這個控制碼時，應用程式必須呼叫 **CloseTouchInputHandle** 來釋放與此控制碼相關聯的進程記憶體。 如果無法這麼做，可能會導致應用程式記憶體流失。

請注意，在訊息傳遞至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)之後，這個參數中的觸控輸入控制碼不再有效。 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 將會關閉並使此控制碼失效。

另請注意，在使用 [**PostMessage**](sendmessage--postmessage--and-related-functions.md)、 **SendMessage** 或其中一個變體轉送訊息之後，此參數中的觸控輸入控點將不再有效。 這些函式會關閉並使此控制碼失效。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

如果應用程式未處理訊息，則必須呼叫 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)。 未這樣做會導致應用程式流失記憶體，因為觸控輸入控制碼未關閉，且相關聯的進程記憶體未釋出。

## <a name="remarks"></a>備註

**WM \_觸控** 訊息不遵守 windows 的 **HTTRANSPARENT** 區域。 如果視窗傳回 **HTTRANSPARENT** 來回應 **WM \_ NCHITTEST** 訊息，則滑鼠訊息會移至父系，而 **WM \_ 觸控** 訊息會直接移至視窗。

## <a name="examples"></a>範例

下列程式碼範例示範如何取得與此訊息相關聯的詳細觸控輸入資訊。


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> <dt>

[操作和慣性程式設計指南](manipulation-and-inertia.md)
</dt> <dt>

[Windows觸控輸入程式設計指南](guide-multi-touch-input.md)
</dt> </dl>

 

