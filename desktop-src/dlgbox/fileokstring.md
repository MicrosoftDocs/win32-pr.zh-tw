---
title: 'FILEOKSTRING message (Commdlg) '
description: 當使用者指定檔案名，然後按一下 [確定] 按鈕時，[開啟] 或 [另存新檔] 對話方塊會將已註冊的 FILEOKSTRING 訊息傳送至您的攔截程式 OFNHookProc。
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- FILEOKSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61208ddebc63f1186c2947416e451231f0bea24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466817"
---
# <a name="fileokstring-message"></a>FILEOKSTRING 訊息

\[從 Windows Vista 開始，[[一般專案] 對話方塊](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]

當使用者指定檔案名，然後按一下 [**確定]** 按鈕時，[**開啟**] 或 [**另存** 新檔] 對話方塊會將已註冊的 **FILEOKSTRING** 訊息傳送至您的攔截程式 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)。 攔截程式可以接受檔案名，並允許對話方塊關閉或拒絕檔案名，並強制對話方塊維持開啟狀態。


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的指標。 此結構的 **lpstrFile** 成員包含使用者所指定的磁片磁碟機、路徑和檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果攔截程式傳回零，則 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊會接受指定的檔案名並關閉。

如果攔截程式傳回非零值，[ **開啟** ] 或 [ **另存** 新檔] 對話方塊會拒絕指定的檔案名並保持開啟狀態。

## <a name="remarks"></a>備註

攔截程式必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **FILEOKSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **FILEOKSTRINGW** (Unicode) 和 **FILEOKSTRINGA** (ANSI) <br/>                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CDN \_ FILEOK**](cdn-fileok.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 

