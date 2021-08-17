---
title: 'WM_UNINITMENUPOPUP 訊息 (Winuser .h) '
description: 當下拉式選單或子功能表已終結時傳送。
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7356c0aa4aa62521d2ab998773d07b8aa1a107c92b541c556756a567d31a09a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971787"
---
# <a name="wm_uninitmenupopup-message"></a>WM \_ UNINITMENUPOPUP 訊息

當下拉式選單或子功能表已終結時傳送。


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

功能表的控制碼

</dd> <dt>

*lParam* 
</dt> <dd>

高序位單字會識別已終結的功能表。 目前，這個參數只能是 (視窗功能表) 的 **MF \_ SYSMENU** 。

</dd> </dl>

## <a name="remarks"></a>備註

如果應用程式收到 [**wm \_ INITMENUPOPUP**](wm-initmenupopup.md) 訊息，則會收到 **wm \_ UNINITMENUPOPUP** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

