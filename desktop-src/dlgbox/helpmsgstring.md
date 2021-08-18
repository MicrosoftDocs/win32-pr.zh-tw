---
title: 'HELPMSGSTRING message (Commdlg) '
description: 當使用者按一下 [說明] 按鈕時，通用的對話方塊會將已註冊的 HELPMSGSTRING 訊息傳送至其擁有者視窗的視窗程式。
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- HELPMSGSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8a446164bb7ae51d36d1a89219f6c3b84eff74b9af3a40c2121b3bd205a581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741738"
---
# <a name="helpmsgstring-message"></a>HELPMSGSTRING 訊息

當使用者按一下 [說明 **] 按鈕時**，通用的對話方塊會將已註冊的 **HELPMSGSTRING** 訊息傳送至其擁有者視窗的視窗程式。


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

通用對話方塊的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

通用對話方塊之初始化結構的指標。 此結構可以是 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)、 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)、 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)、 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)、 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 或 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

您必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **HELPMSGSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。

當您建立對話方塊時，請使用初始化結構的 **hwndOwner** 成員來識別要接收 **HELPMSGSTRING** 訊息的視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HELPMSGSTRINGW** (Unicode) 和 **HELPMSGSTRINGA** (ANSI) <br/>                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CDN \_説明**](cdn-help.md)
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 

