---
title: 'COLOROKSTRING message (Commdlg) '
description: 當使用者選取色彩，然後按一下 [確定] 按鈕時，[色彩] 對話方塊會將已註冊的 COLOROKSTRING 訊息傳送至您的掛勾程式 CCHookProc。
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- COLOROKSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103649"
---
# <a name="colorokstring-message"></a>COLOROKSTRING 訊息

當使用者選取色彩，然後按一下 [**確定]** 按鈕時，[**色彩**] 對話方塊會將已註冊的 **COLOROKSTRING** 訊息傳送至您的掛勾程式 [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)。 攔截程式可以接受色彩，並允許對話方塊關閉或拒絕色彩，然後強制對話方塊保持開啟狀態。


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)結構的指標。 此結構的 **rgbResult** 成員包含所選色彩的 RGB 色彩值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果攔截程式傳回零，[ **色彩** ] 對話方塊會接受選取的色彩並關閉。

如果攔截程式傳回非零值，[ **色彩** ] 對話方塊會拒絕選取的色彩並保持開啟狀態。

## <a name="remarks"></a>備註

攔截程式必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **COLOROKSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **COLOROKSTRINGW** (Unicode) 和 **COLOROKSTRINGA** (ANSI) <br/>                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 

