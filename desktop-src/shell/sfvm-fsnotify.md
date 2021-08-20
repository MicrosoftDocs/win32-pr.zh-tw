---
description: 通知回呼物件，該事件發生了會影響其中一個專案的事件。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_FSNOTIFY 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93aab69cd4d4a49cc9af4601c22196d498f16e281639b96feda2d1e857fdca72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048660"
---
# <a name="sfvm_fsnotify-message"></a>SFVM \_ FSNOTIFY 訊息

通知回呼物件，該事件發生了會影響其中一個專案的事件。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppidl* \[在\]
</dt> <dd>

受影響專案之 PIDL 的指標。

</dd> <dt>

*lEvent* \[在\]
</dt> <dd>

指出發生之事件的 SHCNE 值。 如需可能值的清單，請參閱 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
