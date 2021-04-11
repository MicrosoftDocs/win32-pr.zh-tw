---
description: 傳送至最小化的 (iconic) 視窗。
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: 'WM_QUERYDRAGICON 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319208"
---
# <a name="wm_querydragicon-message"></a>WM \_ QUERYDRAGICON 訊息

傳送至最小化的 (iconic) 視窗。 視窗即將由使用者拖曳，但沒有為其類別定義的圖示。 應用程式可以將控制碼傳回至圖示或游標。 當使用者拖曳圖示時，系統會顯示此游標或圖示。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

應用程式應該會將控制碼傳回給系統在使用者拖曳圖示時所要顯示的游標或圖示。 游標或圖示必須與顯示驅動程式的解析度相容。 如果應用程式傳回 **Null**，系統就會顯示預設資料指標。

## <a name="remarks"></a>備註

當使用者拖曳沒有類別圖示的視窗圖示時，系統會將圖示取代為預設游標。 如果應用程式需要在拖曳期間顯示不同的資料指標，它必須傳回與顯示器驅動程式解析度相容之游標或圖示的控制碼。 如果應用程式將控制碼傳回至色彩游標或圖示，系統會將游標或圖示轉換成黑色和白色。 應用程式可以呼叫 [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) 或 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) 函式，以從可執行檔的 ( .exe) 檔案中的資源載入資料指標或圖示，並取得此控制碼。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **布林** 值，並直接傳回值。 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)函數所設定的 **DWL \_ MSGRESULT** 值會被忽略。

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

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
