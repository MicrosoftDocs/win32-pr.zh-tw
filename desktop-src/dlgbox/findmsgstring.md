---
title: 'FINDMSGSTRING message (Commdlg) '
description: 當使用者按一下 [尋找下一個]、[取代] 或 [全部取代] 按鈕，或關閉對話方塊時，[尋找或取代] 對話方塊會將 FINDMSGSTRING 註冊的訊息傳送至其擁有者視窗的視窗程式。
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- FINDMSGSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509307"
---
# <a name="findmsgstring-message"></a>FINDMSGSTRING 訊息

當使用者按一下 [**尋找下一個**]、[**取代**] 或 [**全部取代**] 按鈕，或關閉對話方塊時，[**尋找** 或 **取代**] 對話方塊會將 **FINDMSGSTRING** 註冊的訊息傳送至其擁有者視窗的視窗程式。


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的指標。 此結構的成員包含最新的使用者輸入，包括要搜尋的字串、取代字串 (是否有任何) 和搜尋和取代選項。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

您必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **FINDMSGSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。

當您建立對話方塊時，請使用 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **hwndOwner** 成員來識別要接收 **FINDMSGSTRING** 訊息的視窗。

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)結構的 **flags** 成員包含下列其中一個旗標，以指出造成訊息的事件。



| 旗標                            | 意義                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_DIALOGTERM** (0x00000040)  | 對話方塊正在關閉。 擁有者視窗處理此訊息之後，對話方塊的控制碼將不再有效。                                                                                    |
| **FR \_FINDNEXT** (0x00000008)    | 使用者按一下 [**尋找** 或 **取代**] 對話方塊中的 [**尋找下一個]** 按鈕。 **LpstrFindWhat** 成員會指定要搜尋的字串。                                                         |
| **FR \_取代** (0x00000010)     | 使用者按一下 [**取代**] 對話方塊中的 [**取代**] 按鈕。 **LpstrFindWhat** 成員會指定要取代的字串，而 **lpstrReplaceWith** 成員會指定取代字串。     |
| **FR \_型全部型** (0x00000020)  | 使用者按一下 [**取代**] 對話方塊中的 [**全部取代**] 按鈕。 **LpstrFindWhat** 成員會指定要取代的字串，而 **lpstrReplaceWith** 成員會指定取代字串。 |



 

如果是 [ **尋找下一個]** 或 [ **取代全部** ] 訊息， **旗標** 成員可以包含下列一或多個旗標，以表示搜尋選項。



| 旗標                           | 意義                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_向下** (0x00000001)       | 如果設定，則會選取 [方向] 選項按鈕的 **向下** 按鈕，表示使用者想要從目前的位置搜尋至檔的結尾。 如果未設定 **FR \_ DOWN** ，則會選取 [ **向上** ] 按鈕，讓使用者想要搜尋檔的開頭。       |
| **FR \_MATCHCASE** (0x00000004)  | 如果設定，則會選取 [ **符合大小寫** ] 核取方塊，表示使用者想要搜尋區分大小寫。 如果未設定 **FR \_ MATCHCASE** ，則不會選取此核取方塊，因此搜尋應該不區分大小寫。                                                                         |
| **FR \_WHOLEWORD** (0x00000002)  | 如果設定，則會選取 [ **僅符合全字** 組] 核取方塊，表示使用者只想搜尋符合搜尋字串的全字組。 如果未設定 **FR \_ WHOLEWORD** ，則不會選取此核取方塊，所以您也應該搜尋符合搜尋字串的文字片段。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **FINDMSGSTRINGW** (Unicode) 和 **FINDMSGSTRINGA** (ANSI) <br/>                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

 

