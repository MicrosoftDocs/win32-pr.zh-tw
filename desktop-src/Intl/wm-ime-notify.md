---
description: 傳送至應用程式，以通知它對 IME 視窗的變更。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: 'WM_IME_NOTIFY 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971221"
---
# <a name="wm_ime_notify-message"></a>WM_IME_NOTIFY 訊息

傳送至應用程式，以通知它對 IME 視窗的變更。 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
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

命令。 這個參數可以是下列其中一個值。

<dl>
<dd><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></dd> 
<dd><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></dd> 
<dd><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></dd> 
<dd><a href="imn-guideline.md">IMN_GUIDELINE</a></dd> 
<dd><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></dd> 
<dd><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></dd> 
<dd><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></dd> 
<dd><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></dd> 
<dd><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></dd> 
<dd><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></dd> 
<dd><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></dd> 
<dd><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

命令特有的資料，其格式取決於 *wParam* 參數的值。 如需詳細資訊，請參閱每個命令的說明文件。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值取決於傳送的命令。

## <a name="remarks"></a>備註

如果應用程式負責管理 IME 視窗，則會處理此訊息。

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

[IMN_CHANGECANDIDATE](imn-changecandidate.md)
</dt> <dt>

[IMN_CLOSECANDIDATE](imn-closecandidate.md)
</dt> <dt>

[IMN_CLOSESTATUSWINDOW](imn-closestatuswindow.md)
</dt> <dt>

[IMN_GUIDELINE](imn-guideline.md)
</dt> <dt>

[IMN_OPENCANDIDATE](imn-opencandidate.md)
</dt> <dt>

[IMN_OPENSTATUSWINDOW](imn-openstatuswindow.md)
</dt> <dt>

[IMN_SETCANDIDATEPOS](imn-setcandidatepos.md)
</dt> <dt>

[IMN_SETCOMPOSITIONFONT](imn-setcompositionfont.md)
</dt> <dt>

[IMN_SETCOMPOSITIONWINDOW](imn-setcompositionwindow.md)
</dt> <dt>

[IMN_SETCONVERSIONMODE](imn-setconversionmode.md)
</dt> <dt>

[IMN_SETOPENSTATUS](imn-setopenstatus.md)
</dt> <dt>

[IMN_SETSENTENCEMODE](imn-setsentencemode.md)
</dt> <dt>

[IMN_SETSTATUSWINDOWPOS](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
