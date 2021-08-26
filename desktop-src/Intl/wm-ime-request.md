---
description: 傳送至應用程式以提供命令和要求資訊。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: 'WM_IME_REQUEST 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d73f1f920efb2908104304fcbc08fd19d648e52fdb737f12027b47436531eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927628"
---
# <a name="wm_ime_request-message"></a>WM_IME_REQUEST 訊息

傳送至應用程式以提供命令和要求資訊。 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
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

命令。 這個參數的值可以是下列其中一個：

<dl> 
<dd><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></dd> 
<dd><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></dd> 
<dd><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></dd> 
<dd><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></dd> 
<dd><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></dd> 
<dd><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></dd> 
<dd><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

命令特有的資料。 如需詳細資訊，請參閱每個命令的描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回命令特定的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                                                      |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) ;</dt><dt>Imm (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員訊息](input-method-manager-messages.md)
</dt> <dt>

[IMR_CANDIDATEWINDOW](imr-candidatewindow.md)
</dt> <dt>

[IMR_COMPOSITIONFONT](imr-compositionfont.md)
</dt> <dt>

[IMR_COMPOSITIONWINDOW](imr-compositionwindow.md)
</dt> <dt>

[IMR_CONFIRMRECONVERTSTRING](imr-confirmreconvertstring.md)
</dt> <dt>

[IMR_DOCUMENTFEED](imr-documentfeed.md)
</dt> <dt>

[IMR_QUERYCHARPOSITION](imr-querycharposition.md)
</dt> <dt>

[IMR_RECONVERTSTRING](imr-reconvertstring.md)
</dt> </dl>

 

 
