---
description: 由檔案管理員延伸模組 (或其他應用程式所傳送) ，使檔案管理員重載 Winfile.ini 檔的附加元件區段中所列的所有擴充 Dll \[ \] 。
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: 'FM_RELOAD_EXTENSIONS 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973229"
---
# <a name="fm_reload_extensions-message"></a>FM \_ 重載 \_ 延伸模組訊息

由檔案管理員延伸模組 (或其他應用程式所傳送) ，使檔案管理員重載 Winfile.ini 檔的附加元件區段中所列的所有擴充 Dll \[ \] 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

其他應用程式可以使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式將此訊息傳送至檔案管理員。 若要取得適當的檔案管理員視窗控制碼，應用程式可以在 FindWindow 函式的呼叫中指定 "WFS \_ Frame [](/windows/win32/api/winuser/nf-winuser-findwindowa) " 作為 *lpszClassName* 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
