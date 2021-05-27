---
title: 'SHAREVISTRING message (Commdlg) '
description: '[開啟] 或 [另存新檔] 對話方塊會將已註冊的 SHAREVISTRING 訊息傳送至您的攔截程式 OFNHookProc，如果當使用者按一下 [確定] 按鈕時，所選取的檔案發生共用違規。'
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- SHAREVISTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043bed9edd08269e4e030482cbd44debea3a3695
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548763"
---
# <a name="sharevistring-message"></a>SHAREVISTRING 訊息

\[從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]

[ **開啟** ] 或 [ **另存** 新檔] 對話方塊會將已註冊的 **SHAREVISTRING** 訊息傳送至您的攔截程式 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)，如果當使用者按一下 [ **確定]** 按鈕時，所選取的檔案發生共用違規。


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的指標。 此結構的 **lpstrFile** 成員包含造成共用違規的檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

攔截程式必須傳回下列其中一個值，以指出對話方塊應該如何處理共用違規。



| 傳回碼/值                                                                                                                                           | Description                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | 接受檔案名<br/>                                                                                            |
| <dl> <dt>**OFN \_SHARENOWARN**</dt> <dt>1</dt> </dl>      | 拒絕檔案名，但不警告使用者。 應用程式會負責顯示警告訊息。<br/> |
| <dl> <dt>**OFN \_SHAREWARN**</dt> <dt>0</dt> </dl>        | 拒絕檔案名，並顯示一則警告訊息， (與沒有攔截程式) 的結果相同。<br/>       |



 

## <a name="remarks"></a>備註

攔截程式必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **SHAREVISTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。

只有當您在建立對話方塊時未在 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **旗標** 成員中指定 **OFN \_ SHAREAWARE** 旗標時，對話方塊才會傳送 **SHAREVISTRING** 註冊的訊息。

如果攔截程式傳回未定義的值，對話方塊會以 **OFN \_ SHAREWARN** 的方式回應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **SHAREVISTRINGW** (Unicode) 和 **SHAREVISTRINGA** (ANSI) <br/>                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

