---
title: 'WM_INPUT_DEVICE_CHANGE 訊息 (Winuser .h) '
description: 傳送至已註冊要接收原始輸入的視窗。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104024269"
---
# <a name="wm_input_device_change-message"></a>WM_INPUT_DEVICE_CHANGE 訊息

## <a name="description"></a>Description

傳送至已註冊要接收原始輸入的視窗。 

只有在應用程式使用[RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice)旗標呼叫[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)之後，才可以使用原始輸入通知。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>參數

<dl> <dt>

*wParam*

</dt> <dd>

類型： **WPARAM**

此參數可以是下列其中一個值。

| 值                    | 意義                                    |
|--------------------------|--------------------------------------------|
| **GIDC \_ 抵達** </br>1 | 系統已新增新的裝置。 </br> 您可以呼叫 [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) 來取得有關裝置的詳細資訊。 |
| **GIDC \_ 移除** </br>2 | 裝置已從系統中移除。 |

</dd> <dt>

*lParam* 

</dt> <dd>

類型： **LPARAM**

原始輸入裝置的 **控制碼** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="see-also"></a>另請參閱

**概念**

[原始輸入](/windows/desktop/inputdev/raw-input)

**參考**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[RAWINPUTDEVICE 結構](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

