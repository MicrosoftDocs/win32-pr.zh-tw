---
description: 當視窗啟用時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: 'WM_IME_SETCONTEXT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191379"
---
# <a name="wm_ime_setcontext-message"></a>WM \_ 輸入法 \_ SETCONTEXT 訊息

當視窗啟用時，傳送至應用程式。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
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

如果視窗為使用中，**則為 TRUE** ，否則為 **FALSE** 。

</dd> <dt>

*lParam* 
</dt> <dd>

顯示選項。 這個參數可以有下列一或多個值。



| 值                                                                                                                                                                                                   | 意義                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**ISC \_ SHOWUICOMPOSITIONWINDOW**</dt> </dl> | 依使用者介面視窗顯示撰寫視窗。<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**ISC \_ SHOWUIGUIDWINDOW**</dt> </dl>                      | 依使用者介面視窗顯示 [節目表] 視窗。<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**ISC \_ SHOWUISOFTKBD**</dt> </dl>                               | 依使用者介面視窗顯示 [螢幕小鍵盤]。<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**ISC \_ SHOWUICANDIDATEWINDOW**</dt> </dl>       | 依使用者介面視窗顯示索引0的候選視窗。<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt> </dl>                                                                                        | 依使用者介面視窗顯示索引1的候選視窗。<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt> </dl>                                                                                        | 依使用者介面視窗顯示索引2的候選視窗。<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt> </dl>                                                                                        | 依使用者介面視窗顯示索引3的候選視窗。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 或 [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)所傳回的值。

## <a name="remarks"></a>備註

如果應用程式已建立 IME 視窗，則應該呼叫 [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)。 否則，它應該會將此訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。

如果應用程式繪製組合視窗，預設的 IME 視窗就不需要顯示其撰寫視窗。 在此情況下，應用程式必須先從 *lParam* 參數清除 **ISC \_ SHOWUICOMPOSITIONWINDOW** 值，然後再將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)或 [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)。 若要顯示特定的使用者介面視窗，應用程式應該移除對應的值，使 IME 不會顯示該值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                                                      |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) ;</dt><dt>Imm (包括 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員訊息](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
