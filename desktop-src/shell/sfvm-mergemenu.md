---
description: 允許回呼物件將功能表項目合併到 Windows 檔案總管功能表中。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_MERGEMENU 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5f6838b3c2ee845794bfa506beada2b7092f1bb918438f820f0e77d6b6543dc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111168"
---
# <a name="sfvm_mergemenu-message"></a>SFVM \_ MERGEMENU 訊息

允許回呼物件將功能表項目合併到 Windows 檔案總管功能表中。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInfo* \[擴展\]
</dt> <dd>

[**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo)結構，其中包含將專案合併到功能表中所需的資訊。

</dd> </dl>

## <a name="remarks"></a>備註

此訊息基本上與自訂資料夾檢視中的 [**IShellBrowser：： InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) 和 [**IShellBrowser：： SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) 具有相同的用途。 如需進一步討論，請參閱 *使用 IShellBrowser 來與*[執行資料夾檢視](../lwef/nse-folderview.md)的 Windows 檔案總管一節。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
