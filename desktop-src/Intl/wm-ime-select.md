---
description: 當作業系統即將變更目前的輸入法時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: 'WM_IME_SELECT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986353"
---
# <a name="wm_ime_select-message"></a>WM \_ 輸入法 \_ 選取訊息

當作業系統即將變更目前的輸入法時，傳送至應用程式。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>

*wParam* 
</dt> <dd>

選取指標。 如果選取了指定的輸入法，此參數會指定 **TRUE** 。 如果不再選取指定的輸入法，參數會設為 **FALSE** 。

</dd> <dt>

*lParam* 
</dt> <dd>

與 IME 相關聯的輸入地區設定識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

已建立 IME 視窗的應用程式應該將此訊息傳遞至該視窗，讓它可以將鍵盤配置控制碼抓取到新選取的輸入。

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會藉由將資訊傳遞至預設 IME 視窗來處理此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員訊息](input-method-manager-messages.md)
</dt> </dl>

 

 
