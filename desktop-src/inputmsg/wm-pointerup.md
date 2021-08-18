---
title: WM_POINTERUP 訊息
description: 當在視窗的工作區上建立連絡人的指標中斷連絡人時張貼。
ms.assetid: 3bdc38da-227c-4be1-bf0b-99704b8a0111
keywords:
- WM_POINTERUP 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5bf811501d189abef127e2b191e159518654650bf569cd2abdad42d7471eb1d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756796"
---
# <a name="wm_pointerup-message"></a>WM_POINTERUP 訊息

當在視窗的工作區上建立連絡人的指標中斷連絡人時張貼。 此輸入訊息會以指標所用的視窗為目標，此時指標會以隱含方式捕捉至視窗，讓視窗繼續接收輸入訊息，包括指標的 **WM_POINTERUP** 通知，直到它中斷連絡人為止。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

> \[!重要\]  
> 桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。

 


```C++
#define WM_POINTERUP                  0x0247
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含指標的相關資訊。 使用下列宏從 wParam 參數取出資訊。

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼。
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指出此訊息是否代表新指標所產生之第一個輸入的旗標。
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：此旗標會指出此訊息是否會在其存留期間由指標產生。 未在指出指標具有左方偵測範圍的訊息上設定此旗標
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：此旗標會指出此訊息是否由與視窗介面聯繫的指標所產生。 此旗標不會設定在指出暫留指標的訊息上。
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：表示此指標已指定為主要指標。
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指出是否有主要動作的旗標。
    -   這類似于按下滑鼠左鍵。
    -   當觸控指標與數位板介面聯繫時，會有此設定。
    -   當畫筆指標與數位板介面聯繫時，如果未按下任何按鈕，就會有此設定。
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指出是否有次要動作的旗標。
    -   這類似于滑鼠右鍵向下按鈕。
    -   當畫筆指標與數位板介面聯繫時，如果已按下畫筆圓筒按鈕，就會有此設定。
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：旗標，指出是否有一或多個以指標類型為基礎的三個動作;想要回應第三個動作的應用程式必須抓取指標類型的特定資訊，以判斷要按下的第三個按鈕。 例如，應用程式可以藉由呼叫 [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) 和檢查指定按鈕狀態的旗標，判斷畫筆的按鈕狀態。
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指出指定的指標是否採取第四個動作的旗標。 想要回應第四個動作的應用程式必須抓取指標類型的特定資訊，以判斷是否按下第一個擴充滑鼠 (XButton1) 按鈕。
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ： [**旗**](pointer-flags-contants.md) 標，指出指定的指標是否花費第五個動作。 想要回應第五個動作的應用程式必須抓取指標類型的特定資訊，以判斷是否按下第二個擴充滑鼠 (XButton2) 按鈕。

    如需詳細資訊，請參閱 [**指標旗標**](pointer-flags-contants.md) 。

    > [!Note]  
    > 停留指標沒有設定按鈕旗標。 這類似于未按下滑鼠按鍵的滑鼠移動。 應用程式可以藉由呼叫 [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) 和檢查指定按鈕狀態的旗標，來決定暫留畫筆的按鈕狀態。

     

</dd> <dt>

*lParam* 
</dt> <dd>

包含指標的點位置。

> [!Note]  
> 因為指標可能會透過非一般區域與裝置聯繫，所以這個點位置可以簡化更複雜的指標區域。 如果可能的話，應用程式應該使用完整的指標區域資訊，而不是點位置。

 

您可以使用下列宏來取出點的實際螢幕座標。

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam) (LPARAM) ： X (水準點) 座標。
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam) (LPARAM) ： Y (垂直點) 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。

## <a name="remarks"></a>備註

> \[!重要\]  
> 當視窗失去指標的捕獲，且收到 [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) 通知時，通常不會收到任何進一步的通知。 基於這個理由，請務必不要根據平均配對的 [**WM_POINTERDOWN**](wm-pointerdown.md) / **WM_POINTERUP** 或 [**WM_POINTERENTER**](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md)通知來做出任何假設。

 

每個指標在其存留期內都有唯一的指標識別碼。 指標的存留期會在第一次偵測到時開始。

如果偵測到停留指標，就會產生 [**WM_POINTERENTER**](wm-pointerenter.md) 訊息。 如果偵測不到停留指標，則會產生 [**WM_POINTERDOWN**](wm-pointerdown.md) 訊息，後面接著 **WM_POINTERENTER** 訊息。

在其存留期內，指標可能會在其停留或聯繫時產生一系列的 [**WM_POINTERUPDATE**](wm-pointerupdate.md) 訊息。

指標的存留期會在不再偵測到它時結束。 這會產生 [**WM_POINTERLEAVE**](wm-pointerleave.md) 的訊息。

當指標中止時，會設定 [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) 。

當非捕捉的指標移至視窗的範圍之外時，也可能會產生 [**WM_POINTERLEAVE**](wm-pointerleave.md) 訊息。

若要取得指標的水準和垂直位置，請使用下列程式：

使用下列程式碼來取得水準和垂直位置：


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



[**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints)宏也可以用來將 lParam 參數轉換成 [**點**](/previous-versions//dd162808(v=vs.85))結構。

[**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate)函數可以用來判斷與此訊息相關聯的鍵盤輔助按鍵狀態。 例如，若要偵測是否已按下 ALT 鍵，請檢查 **GetKeyState** (VK_MENU) &lt; 0。

如果應用程式不會處理此訊息， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 可能會產生一或多個 [**WM_GESTURE**](../wintouch/wm-gesture.md)訊息（如果此和中的輸入順序可能會被辨識為手勢）。 如果無法辨識手勢， **DefWindowProc** 可能會產生滑鼠輸入。

如果應用程式選擇性地取用一些指標輸入，並將 rest 傳遞給 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)，則產生的行為是未定義的。

您可以使用 [**GetPointerInfo**](/previous-versions/windows/desktop/api) 函式來取得與此訊息相關的進一步資訊。

## <a name="examples"></a>範例

下列程式碼範例會示範如何取出 jumpbox 此訊息的相關指標的 x 和 y 位置。


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

// process pointer up, similar to mouse button up
```



下列程式碼範例顯示如何取得與此訊息相關聯的指標識別碼。


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &pointerInfo))
{
    
// failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}


```



下列程式碼範例顯示如何處理與此訊息相關聯的不同指標類型。


```c++
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> <dt>

**參考**
</dt> <dt>

[**指標旗標**](pointer-flags-contants.md)
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>
