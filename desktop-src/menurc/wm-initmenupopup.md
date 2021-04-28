---
title: 'WM_INITMENUPOPUP 訊息 (Winuser .h) '
description: WM_INITMENUPOPUP 訊息-在下拉式功能表或子功能表即將變成作用中時傳送。 這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d850547d57596dd36b36b941d1782c2aee1f5b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092516"
---
# <a name="wm_initmenupopup-message"></a>WM \_ INITMENUPOPUP 訊息

當下拉功能表或子功能表即將變成作用中時傳送。 這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

下拉式功能表或子功能表的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組會指定開啟下拉式功能表或子功能表之功能表項目的以零為起始的相對位置。

高序位單字指出下拉式功能表是否為 [視窗] 功能表。 如果功能表是 [視窗] 功能表，此參數為 **TRUE**;否則為 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ INITMENU**](wm-initmenu.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤加速器](keyboard-accelerators.md)
</dt> </dl>

 

