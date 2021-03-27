---
description: 當使用者按下功能表或工具列命令專案上的 F1 時，傳送至檔案管理員延伸模組 DLL 程式。 擴充功能應該呼叫 WinHelp，並將該函式的 hwnd 參數設定為延伸模組的 hwnd 參數值。
title: 'FMEVENT_HELPMENUITEM 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: c20b5828a6e2362b9b9c13fc9b2986b0ea7b5fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971917"
---
# <a name="fmevent_helpmenuitem-message"></a>FMEVENT \_ HELPMENUITEM 訊息

當使用者按下功能表或工具列命令專案上的 F1 時，傳送至檔案管理員延伸模組 DLL 程式。 擴充功能應該呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)，並將該函式的 *hwnd* 參數設定為延伸模組的 *hwnd* 參數值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*uItem* 
</dt> <dd>

識別所需說明之功能表或工具列命令專案的值。 擴充程式會使用這個值來判斷呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)的最佳方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果延伸 DLL 程式處理此訊息，則應該傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPSTRING**](fmevent-helpstring.md)
</dt> </dl>

 

 




