---
description: 當使用者執行筆觸時傳送。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: 'WM_TABLET_FLICK 訊息 (Tpcshrd .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191296"
---
# <a name="wm_tablet_flick-message"></a>WM \_ TABLET \_ 筆鋒訊息

當使用者執行筆觸時傳送。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**筆鋒 \_ 資料結構**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)，其中包含所發生之筆觸的相關資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

指定手寫筆筆觸發生位置的 [**筆鋒 \_ 點結構**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) 。

</dd> </dl>

## <a name="remarks"></a>備註

筆觸是一個單向畫筆手勢，要求使用者在快速、直接撥動的動作中與數位板聯繫。 筆勢的特性是高速和高度的 straightness。 筆觸是由其方向來識別。 您可以用對應至基線和次要羅盤方向的八個方向來進行筆觸。

當筆觸出現時，Windows 會先傳送 **WM \_ TABLET \_ 筆鋒** 訊息（視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函式接收）來通知應用程式。 傳回「 **筆觸 \_ WM \_ 處理的 \_ 遮罩** 常數」（如 [筆觸常數](flicks-constants.md)中所述），以表示應用程式已回應 **WM \_ TABLET \_ 筆鋒** 訊息。 如果應用程式未傳回筆觸 **\_ WM \_ 處理的 \_ 遮罩**，則 Windows 會根據與手寫筆筆觸相關聯的動作傳送後續通知（例如 [**Wm \_ APPCOMMAND**](../inputdev/wm-appcommand.md)、 [**wm \_ VSCROLL**](../controls/wm-vscroll.md)或 [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md)），來執行筆觸控制台中指定的預設動作。

處理 **WM \_ TABLET 筆觸 \_** 訊息時，請特別小心。 **WM \_TABLET \_ 筆觸** 是經由 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) 函式傳遞。 如果您呼叫 COM 介面上的方法，該物件必須在相同的進程中。 如果不是，COM 會擲回例外狀況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Tpcshrd。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**筆鋒 \_ 資料結構**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**wm \_ tablet \_ 筆鋒訊息**](wm-tablet-flick-message.md)
</dt> <dt>

[筆觸手勢](flicks-gestures.md)
</dt> <dt>

[回應觸控筆觸](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
