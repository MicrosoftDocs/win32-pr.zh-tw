---
description: 當屬於與使用中視窗不同的應用程式視窗即將啟動時傳送。 訊息會傳送至應用程式，該應用程式的視窗正在啟動，而應用程式的視窗則會被停用。
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: 'WM_ACTI加值稅EAPP 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985471"
---
# <a name="wm_activateapp-message"></a>WM \_ ACTI加值稅EAPP 訊息

當屬於與使用中視窗不同的應用程式視窗即將啟動時傳送。 訊息會傳送至應用程式，該應用程式的視窗正在啟動，而應用程式的視窗則會被停用。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出視窗是否正在啟用或停用。 如果要啟用視窗，此參數為 **TRUE** 。如果視窗正在停用，則為 **FALSE** 。

</dd> <dt>

*lParam* 
</dt> <dd>

執行緒識別碼。 如果 *wParam* 參數為 **TRUE**，則 *lParam* 是擁有停用視窗之執行緒的識別碼。 如果 *wParam* 為 **FALSE**，則 *lParam* 是擁有要啟用之視窗的執行緒識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

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

[**WM \_ 啟用**](../inputdev/wm-activate.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
