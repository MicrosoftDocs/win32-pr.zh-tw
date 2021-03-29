---
description: SFVM \_ GETDETAILSOF 可能已變更或無法使用。
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: 'SFVM_GETDETAILSOF 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973481"
---
# <a name="sfvm_getdetailsof-message"></a>SFVM \_ GETDETAILSOF 訊息

\[**SFVM \_GETDETAILSOF** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

允許回呼物件提供 Shell 資料夾中專案的詳細資料。 只有在呼叫 [**IShellFolder2：： GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) 失敗，而且沒有可供呼叫的 [**IShellDetails：： GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) 方法時，才使用。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*iColumn* \[在\]
</dt> <dd>

以零為基底的資料行識別碼。

</dd> <dt>

*pDi* \[擴展\]
</dt> <dd>

[**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo)結構的指標，該結構已填入要求的資訊。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 用戶端支援結束<br/>    | Windows XP 含 SP2<br/>                                                      |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
