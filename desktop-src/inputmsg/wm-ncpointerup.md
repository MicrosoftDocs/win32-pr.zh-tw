---
title: WM_NCPOINTERUP 訊息
description: 在視窗的非工作區上建立連絡人的指標中斷連絡人時張貼。
ms.assetid: 4bdc11da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUP 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_NCPOINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a875814b51558c20de47eeee525f6dd35f716fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686176"
---
# <a name="wm_ncpointerup-message"></a>WM_NCPOINTERUP 訊息

在視窗的非工作區上建立連絡人的指標中斷連絡人時張貼。 訊息會以指標所用的視窗為目標，而指標會在該視窗上以隱含方式捕捉至視窗，讓視窗繼續接收指標的輸入，直到它中斷連絡人為止，包括 **WM_NCPOINTERUP** 通知。

如果視窗已捕捉到此指標，則不會張貼此訊息。 相反地， [**WM_POINTERUP**](wm-pointerup.md) 會張貼到已捕獲此指標的視窗。

> \[!重要\]  
> 桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。

 


```C++
#define WM_NCPOINTERUP               0x0243
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含指標識別碼和其他資訊。 使用下列宏來取得此資訊。

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) (wParam) ：處理 [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) 訊息時所傳回的點擊測試值。

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

如果應用程式未處理此訊息， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 可能會根據訊息中包含的點擊測試結果，執行一或多個系統動作。 一般而言，應用程式應該不需要處理此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> </dl>

 

