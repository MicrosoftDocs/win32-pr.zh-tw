---
title: 'WM_MOUSEHWHEEL 訊息 (Winuser .h) '
description: 當滑鼠的水準滾輪傾斜或旋轉時，傳送至使用中視窗。
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- WM_MOUSEHWHEEL 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de63d214d087cb804c3973fbba6a90c46955506ebddf5da57a7578d224edb803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451488"
---
# <a name="wm_mousehwheel-message"></a>WM \_ MOUSEHWHEEL 訊息

當滑鼠的水準滾輪傾斜或旋轉時，傳送至使用中視窗。 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將訊息傳播至視窗的父代。 訊息不應該有內部轉送，因為 **DefWindowProc** 會將它傳播到父鏈上，直到它找到處理它的視窗為止。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

高序位單字表示滾輪旋轉的距離，以重數或 **輪子 \_ DELTA** 的因數表示，其設定為120。 正值表示滾輪已向右旋轉;負數值表示滾輪已向左旋轉。

低序位單字指出是否有不同的虛擬機器碼已關閉。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                                                               | 意義                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_控制項**</dt> <dt>0x0008</dt> </dl>    | CTRL 鍵已關閉。<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt> </dl>    | 左邊的滑鼠按鍵已關閉。<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt> </dl>    | 中間的滑鼠按鍵已關閉。<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt> </dl>    | 滑鼠右鍵已關閉。<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_SHIFT**</dt> <dt>0x0004</dt> </dl>          | SHIFT 鍵已關閉。<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt> </dl> | 第一個 X 按鈕已關閉。<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt> </dl> | 第二個 X 按鈕已關閉。<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字指定指標的 x 座標（相對於畫面的左上角）。

高序位字指定指標的 y 座標（相對於畫面的左上角）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

使用下列程式碼來取得 *wParam* 參數中的資訊。


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



使用下列程式碼來取得水準和垂直位置。


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。 如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。 您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。

> [!IMPORTANT]
> 請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。 具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。

 

滾輪旋轉是 **滾輪 \_ 差異** 的倍數，其設定為120。 這是所要採取動作的臨界值，而其中一個這類動作 (例如，每個差異都應進行滾動一個遞增) 。

差異已設定為120，可讓 Microsoft 或其他廠商建立更精細的解析度滾輪 (例如，無凹槽的自由旋轉滾輪) 在每次旋轉時傳送更多訊息，但每則訊息中的值較小。 若要使用此功能，您可以新增傳入的 delta 值，直到達到 **輪子 \_ delta** 為止 (因此，若為差異旋轉，您會收到相同的回應) ，或滾動部分行以回應更頻繁的訊息。 您也可以選擇您的捲軸細微性，並累計差異直到到達為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windowsx) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**取得 \_ KEYSTATE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**取得 \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**取得 \_ 輪子 \_ DELTA \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**滑鼠 \_ 事件**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**概念**
</dt> <dt>

[滑鼠輸入](mouse-input.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**點**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

