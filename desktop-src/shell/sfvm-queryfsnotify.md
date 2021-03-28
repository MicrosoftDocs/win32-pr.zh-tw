---
description: SFVM \_ QUERYFSNOTIFY 可能已變更或無法使用。
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: 'SFVM_QUERYFSNOTIFY 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195330"
---
# <a name="sfvm_queryfsnotify-message"></a>SFVM \_ QUERYFSNOTIFY 訊息

\[**SFVM \_QUERYFSNOTIFY** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

允許回呼物件註冊資料夾，讓該資料夾的視圖變更會產生通知。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*shcne* \[in、out\]
</dt> <dd>

結構，用來保存要監看事件的專案 PIDL，以及指出是否也應該監看該專案的子資料夾。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 用戶端支援結束<br/>    | Windows XP 含 SP2<br/>                                                      |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
