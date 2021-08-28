---
title: WM_POINTERENTER 訊息
description: 當新指標在視窗上進入偵測範圍時傳送至視窗 (停留) ，或當現有指標在視窗界限內移動時。
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8a0222
keywords:
- WM_POINTERENTER 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: dfb871f232ea04b417b0aa038da1aaf7831a6a8e4d86b3c2888ca7c6e3708553
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602278"
---
# <a name="wm_pointerenter-message"></a>WM_POINTERENTER 訊息

當新指標在視窗上進入偵測範圍時傳送至視窗 (停留) ，或當現有指標在視窗界限內移動時。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

> \[!重要\]  
> 桌面應用程式應該要感知 DPI。 如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。 DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。 如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。

 


```C++
#define WM_POINTERENTER                 0x0249
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含指標識別碼和其他資訊。 使用下列宏來取出 wParam 參數中的特定資訊。

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼。
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指出此訊息是否為新指標所產生的第一則訊息，此指標會輸入偵測範圍 (停留) 。
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指出此訊息是否由未離開偵測範圍的指標所產生。 此旗標一律會針對 **WM_POINTERENTER** 訊息設定。
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

當指標在表面上時，視窗會使用 **WM_POINTERENTER** 通知，將意見反應提供給使用者，或是在指標上方回應指標的存在。

此通知只會傳送至接收指標輸入的視窗。 下表列出傳送此通知的部分情況。



| 動作                                                   | 旗標集合                                                                                                                                         | 傳送至的通知                                 |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| 新指標進入偵測範圍 (停留) 。            | [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)<br/> [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/> | 指標進入偵測範圍的視窗。 |
| 停留在視窗界限內的指標。 | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/>                                                                      | 指標跨越的時間範圍。          |



 

> \[!重要\]  
> 當視窗失去指標的捕獲，且收到 [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) 通知時，通常不會收到任何進一步的通知。 基於這個理由，請務必不要根據平均配對的 [**WM_POINTERDOWN**](wm-pointerdown.md) / [**WM_POINTERUP**](wm-pointerup.md)或 **WM_POINTERENTER** / [**WM_POINTERLEAVE**](wm-pointerleave.md)通知來做出任何假設。

 

當輸入來自滑鼠時，因為滑鼠和指標訊息整合的結果， **WM_POINTERENTER** 不會傳送。

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

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

