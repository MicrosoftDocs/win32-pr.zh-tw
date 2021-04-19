---
title: WM_POINTERLEAVE 訊息
description: 當指標在視窗上離開偵測範圍時傳送至視窗 (停留) 或指標移至視窗界限之外。
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8c1322
keywords:
- WM_POINTERLEAVE 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2ee58fd74f266d067f6211e156d984a3b3d1c477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966330"
---
# <a name="wm_pointerleave-message"></a>WM_POINTERLEAVE 訊息

當指標在視窗上離開偵測範圍時傳送至視窗 (停留) 或指標移至視窗界限之外。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

> \[!重要\]  
> 桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。

 


```C++
#define WM_POINTERLEAVE                 0x024A
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含指標識別碼和其他資訊。 使用下列宏來取得此資訊。

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼。
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指出此訊息是否由未離開偵測範圍的指標所產生。 當指標離開視窗的偵測範圍時，不會設定這個旗標。
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：此旗標會指出此訊息是否由連絡人的指標所產生。 偵測範圍中的指標未設定此旗標 (停留) 。

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

當指標在視窗介面上方時，視窗可以使用 **WM_POINTERLEAVE** 通知來變更模式或停止任何意見反應給使用者。

此通知只會傳送至接收指標輸入的視窗。 下表列出傳送此通知的部分情況。



| 動作                                        | 旗標集合                                                         | 傳送至的通知                                |
|-----------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------|
| 停留指標跨越視窗界限。 | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) | 指標移至其界限外的視窗。  |
| 指標離開偵測範圍。        | N/A                                                               | 指標離開偵測範圍的視窗。 |



 

> \[!重要\]  
> 當視窗失去指標的捕獲，且收到 [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) 通知時，通常不會收到任何進一步的通知。 基於這個理由，請務必不要根據平均配對的 [**WM_POINTERDOWN**](wm-pointerdown.md) / [**WM_POINTERUP**](wm-pointerup.md)或 [**WM_POINTERENTER**](wm-pointerenter.md) / **WM_POINTERLEAVE** 通知來做出任何假設。

 

如果 contact 與輸入數位板保持在一起，且指標在視窗外移動，就不會產生 **WM_POINTERLEAVE** 。 只有當滑鼠停留指標跨越視窗界限或連絡人結束時，才會產生 **WM_POINTERLEAVE** 。

如果輸入是源自于滑鼠裝置， **WM_POINTERLEAVE** 會張貼至張貼的訊息佇列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[訊息](messages.md)
</dt> <dt>

**參考**
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

