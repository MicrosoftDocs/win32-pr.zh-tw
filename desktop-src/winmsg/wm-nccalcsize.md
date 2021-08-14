---
description: 當必須計算視窗工作區的大小和位置時傳送。 藉由處理這個訊息，應用程式可以在視窗的大小或位置變更時，控制視窗工作區的內容。
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: 'WM_NCCALCSIZE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a73b469a920bcba79cc19670a7b9536c1bac9e0b0ffcab7ddf5930b984dae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200074"
---
# <a name="wm_nccalcsize-message"></a>WM \_ NCCALCSIZE 訊息

當必須計算視窗工作區的大小和位置時傳送。 藉由處理這個訊息，應用程式可以在視窗的大小或位置變更時，控制視窗工作區的內容。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

如果 *wParam* 為 **TRUE**，它會指定應用程式應該指出工作區的哪個部分包含有效的資訊。 系統會將有效的資訊複製到新工作區中的指定區域。

如果 *wParam* 為 **FALSE**，則應用程式不需要表示工作區的有效部分。

</dd> <dt>

*lParam* 
</dt> <dd>

如果 *wParam* 為 **TRUE**， *lParam* 會指向 [**NCCALCSIZE \_ PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) 結構，其中包含應用程式可用來計算用戶端矩形新大小和位置的資訊。

如果 *wParam* 為 **FALSE**，則 *lParam* 會指向 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構。 當輸入時，結構會包含視窗的建議視窗矩形。 在結束時，結構應包含對應之視窗工作區的螢幕座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果 *wParam* 參數為 **FALSE**，則應用程式應該傳回零。

如果 *wParam* 為 **TRUE**，則應用程式應該傳回零或下列值的組合。

如果 *wParam* 為 **TRUE** ，且應用程式傳回零，則會保留舊的工作區，並與新工作區的左上角對齊。



| 傳回碼/值                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_ALIGNTOP**</dt> <dt>0x0010</dt> </dl>    | 指定要保留視窗的工作區，並與視窗新位置的頂端對齊。 例如，若要將工作區對齊左上角，請傳回 WVR \_ ALIGNTOP 和 **WVR \_ ALIGNLEFT** 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_ALIGNRIGHT**</dt> <dt>0x0080</dt> </dl>  | 指定要保留視窗的工作區，並與視窗新位置的右邊對齊。 例如，若要將工作區對齊右下角，請傳回 **WVR \_ ALIGNRIGHT** 和 WVR \_ ALIGNBOTTOM 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_ALIGNLEFT**</dt> <dt>0x0020</dt> </dl>   | 指定要保留視窗的工作區，並與視窗新位置的左邊對齊。 例如，若要將工作區對齊左下角，請傳回 **WVR \_ ALIGNLEFT** 和 **WVR \_ ALIGNBOTTOM** 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_ALIGNBOTTOM**</dt> <dt>0x0040</dt> </dl> | 指定要保留視窗的工作區，並與視窗新位置的底部對齊。 例如，若要將工作區對齊左上角，請傳回 WVR \_ ALIGNTOP 和 **WVR \_ ALIGNLEFT** 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_HREDRAW**</dt> <dt>0x0100</dt> </dl>     | 與任何其他值搭配使用（除了 **WVR \_ VALIDRECTS** 以外）時，如果用戶端矩形以水準方式變更大小，就會讓視窗完全重繪。 此值類似于 [CS \_ HREDRAW](about-window-classes.md) 類別樣式<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_VREDRAW**</dt> <dt>0x0200</dt> </dl>     | 與任何其他值搭配使用（除了 **WVR \_ VALIDRECTS**）時，如果用戶端矩形的大小垂直變更，則會讓視窗完全重繪。 此值類似于 [CS \_ VREDRAW](about-window-classes.md) 類別樣式<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_重繪**</dt> <dt>0x0300</dt> </dl>      | 此值會重新繪製整個視窗。 它是 **WVR \_ HREDRAW** 和 **WVR \_ VREDRAW** 值的組合。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_VALIDRECTS**</dt> <dt>0x0400</dt> </dl>  | 這個值表示，在從 [**WM \_ NCCALCSIZE**](wm-nccalcsize.md)傳回時，  \[ NCCALCSIZE PARAMS 結構的 rgrc 1 和 rgrc 2 成員所指定的矩形會 \]  \[ \] 分別包含有效的目的地和來源區域矩形。 [**\_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) 系統會合並這些矩形，以計算要保留的視窗區域。 系統會複製來源矩形內視窗影像的任何部分，並將影像裁剪至目的地矩形。 這兩個矩形都在父相對或螢幕相對座標中。 此旗標無法與任何其他旗標合併。 <br/> 此傳回值可讓應用程式執行更詳盡的用戶端區域保留原則，例如，將工作區的子集集中或保留。<br/> |



 

## <a name="remarks"></a>備註

視是否指定 [cs \_ HREDRAW](about-window-classes.md) 或 cs \_ VREDRAW 類別樣式而定，可能會重新繪製視窗。 這是 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式 (的預設回溯相容性處理，除了上表中所述的一般用戶端矩形計算) 之外。

當 *wParam* 為 **TRUE** 時，只要在未處理 [**NCCALCSIZE \_ PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) 矩形的情況下傳回0，就會使工作區大小調整為視窗的大小，包括視窗框架。 這會從您的視窗中移除視窗框架和標題專案，只留下顯示的工作區。

從 Windows Vista 開始，只要在 *wParam* 為 **TRUE** 時直接傳回0，即可移除標準框架，而不會影響使用 [**DwmExtendFrameIntoClientArea**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea)函數延伸至工作區的框架。 只會移除標準框架。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**NCCALCSIZE \_ 參數**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**矩形**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
