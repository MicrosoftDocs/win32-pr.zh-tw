---
description: 在應用程式的輸入語言變更後，傳送至最上層受影響的視窗。 您應該進行任何應用程式專屬的設定，並將訊息傳遞至 DefWindowProc 函式，此函式會將訊息傳遞給所有的第一層子視窗。
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: 'WM_INPUTLANGCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112845"
---
# <a name="wm_inputlangchange-message"></a>WM \_ INPUTLANGCHANGE 訊息

在應用程式的輸入語言變更後，傳送至最上層受影響的視窗。 您應該進行任何應用程式專屬的設定，並將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，此函式會將訊息傳遞給所有的第一層子視窗。 這些子視窗可以將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，讓它將訊息傳遞給其子視窗，依此類推。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

新地區設定的字元集。

</dd> <dt>

*lParam* 
</dt> <dd>

輸入地區設定識別碼。 如需詳細資訊，請參閱 [語言、地區設定和鍵盤配置](../inputdev/about-keyboard-input.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回非零值。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ INPUTLANGCHANGEREQUEST**](wm-inputlangchangerequest.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
