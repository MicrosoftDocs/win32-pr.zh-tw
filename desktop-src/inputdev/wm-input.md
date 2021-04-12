---
title: 'WM_INPUT 訊息 (Winuser .h) '
description: 傳送至正在取得原始輸入的視窗。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384421"
---
# <a name="wm_input-message"></a>WM \_ 輸入訊息

傳送至正在取得原始輸入的視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>參數

<dl> <dt>

*wParam*

</dt> <dd>

輸入代碼。 使用 [**get \_ RAWINPUT \_ CODE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) 宏來取得值。

可以是下列值之一：

| 值 | 意義 |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**邊緣 \_輸入**</dt> <dt>0</dt> </dl> | 當應用程式在前景時，就會發生輸入。 </br> 應用程式必須呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，讓系統可以執行清除。 |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**邊緣 \_INPUTSINK**</dt> <dt>1</dt> </dl> | 當應用程式不在前景時，就會發生輸入。 |

</dd> <dt>

*lParam* 

</dt> <dd>

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)結構的 **HRAWINPUT** 控制碼，其中包含來自裝置的原始輸入。 若要取得原始資料，請在 [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)的呼叫中使用這個控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

只有在應用程式使用有效的裝置規格呼叫 [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) 時，才可以使用原始輸入。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|-------------------------------------------|
| 最低支援的用戶端 | \[僅限 WINDOWS XP desktop 應用程式\] |
| 最低支援的伺服器 | 僅限 Windows Server 2003 \[ desktop 應用程式\] |
| 標頭 | <dl> <dt>**Winuser (包含) 的 Windows .h**</dt> </dl> |

## <a name="see-also"></a>另請參閱

**參考**

[**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**取得 \_ RAWINPUT 程式 \_ 代碼 \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**概念**

[原始輸入](raw-input.md)
