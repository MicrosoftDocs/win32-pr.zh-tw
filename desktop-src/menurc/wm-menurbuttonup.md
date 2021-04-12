---
title: 'WM_MENURBUTTONUP 訊息 (Winuser .h) '
description: 當使用者放開滑鼠右鍵，而游標位於功能表項目上時傳送。
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317516"
---
# <a name="wm_menurbuttonup-message"></a>WM \_ MENURBUTTONUP 訊息

當使用者放開滑鼠右鍵，而游標位於功能表項目上時傳送。


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

功能表項目以零為起始的索引，也就是用來釋放滑鼠右鍵的功能表項目。

</dd> <dt>

*lParam* 
</dt> <dd>

包含專案之功能表的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

**WM \_ MENURBUTTONUP** 訊息可讓應用程式提供內容相關功能表，也稱為此訊息中指定之功能表項目的快捷方式功能表。 若要顯示功能表項目的內容相關功能表，請使用 **TPM \_ 遞迴** 呼叫 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[功能表總覽](menus.md)
</dt> </dl>

 

 





