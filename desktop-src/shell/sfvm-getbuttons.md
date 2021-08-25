---
description: 允許回呼物件指定要加入至工具列的按鈕。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: 'SFVM_GETBUTTONS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299641ef45d17a6ad1e4d709c3250abe220e297daedabcb563eeba9dcf56262a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008978"
---
# <a name="sfvm_getbuttons-message"></a>SFVM \_ GETBUTTONS 訊息

允許回呼物件指定要加入至工具列的按鈕。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

中的 *idCmdFirst \_ cbtnMax* \[\]
</dt> <dd>

包含使用 [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) 宏封裝到參數中的 2 16 位值。 低序位字組包含初始命令識別碼。 高序位單字包含要加入的按鈕數目（如先前的 [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) 訊息中所指定）。

</dd> <dt>

*pbtn* \[擴展\]
</dt> <dd>

[**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton)結構陣列的位址，每個要新增至工具列的按鈕各有一個位址。

</dd> </dl>

## <a name="remarks"></a>備註

此訊息的前面會有 [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) 訊息。 回呼物件必須處理該訊息，以指定按鈕的數目，以及要在工具列上放置它們的位置。 根據回呼物件回應 **SFVM \_ GETBUTTONINFO** 訊息的方式， *pbtn* 參數所指定的按鈕將會附加到系統資料夾 view 物件的標準按鈕或前面，或是取代標準集。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
