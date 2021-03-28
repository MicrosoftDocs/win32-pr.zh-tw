---
description: 允許回呼物件指定在背景執行緒上列舉專案時顯示動畫。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: 'SFVM_GETANIMATION 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115833"
---
# <a name="sfvm_getanimation-message"></a>SFVM \_ GETANIMATION 訊息

允許回呼物件指定在背景執行緒上列舉專案時顯示動畫。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*phinst* \[擴展\]
</dt> <dd>

應從中載入資源之模組的實例控制碼。

</dd> <dt>

*pwszName* \[擴展\]
</dt> <dd>

以 null 終止的 Unicode 字串指標，其中包含 .avi 檔案的路徑或 AVI 資源的名稱。 或者，此參數可以包含低序位字組中的資源識別碼，以及高序位字組中的0。 若要建立這個值，請使用 [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) 宏。 控制項會從 hinst 所指定的模組載入資源。 AVI 資源必須有 "AVI" 類型。

</dd> </dl>

## <a name="remarks"></a>備註

根據預設，系統資料夾 view 物件會在背景列舉期間顯示「底圖」動畫。

*phinst* 和 *pwszName* 將會傳遞至具有「已 [**\_ 開啟**](../controls/acm-open.md)」訊息的 [動畫控制項](../controls/animation-control-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
