---
title: 'WM_SETCURSOR 訊息 (Winuser .h) '
description: 如果滑鼠導致游標在視窗內移動，且未捕捉到滑鼠輸入，則傳送至視窗。
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025184"
---
# <a name="wm_setcursor-message"></a>WM \_ SETCURSOR 訊息

如果滑鼠導致游標在視窗內移動，且未捕捉到滑鼠輸入，則傳送至視窗。


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含游標的視窗控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

*LParam* 的低序位文字會指定資料指標位置的點擊測試結果。 如需可能的值，請參閱 [WM_NCHITTEST](../inputdev/wm-nchittest.md) 的傳回值。

*LParam* 的高序位單字會指定觸發此事件的滑鼠視窗訊息，例如 [WM_MOUSEMOVE](../inputdev/wm-mousemove.md)。 當視窗進入功能表模式時，此值為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE** 以停止進一步的處理，或傳回 **FALSE** 以繼續。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)函式會在處理之前，將 **WM \_ SETCURSOR** 訊息傳遞至父視窗。 如果父視窗傳回 **TRUE**，則會停止進一步處理。 將訊息傳遞至視窗的父視窗，可讓父視窗控制子視窗中資料指標的設定。 **DefWindowProc** 函式也會使用這個訊息，將資料指標設定為不在工作區中的箭號，如果是在工作區中，則為已註冊的類別游標。 如果 *lParam* 參數的低序位字是 **HTERROR** ，而 *lParam* 的高序位字指定按下其中一個滑鼠按鍵， **DefWindowProc** 就會呼叫 [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) 函數。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**概念**
</dt> <dt>

[游標](cursors.md)
</dt> </dl>

 

