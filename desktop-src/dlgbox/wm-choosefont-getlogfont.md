---
title: 'WM_CHOOSEFONT_GETLOGFONT 訊息 (Commdlg .h) '
description: 應用程式會將 WM \_ CHOOSEFONT \_ GETLOGFONT 訊息傳送至 [字型] 對話方塊，以取得使用者目前字型選取專案的相關資訊。
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- WM_CHOOSEFONT_GETLOGFONT 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966520"
---
# <a name="wm_choosefont_getlogfont-message"></a>WM \_ CHOOSEFONT \_ GETLOGFONT 訊息

應用程式會將 **WM \_ CHOOSEFONT \_ GETLOGFONT** 訊息傳送至 [ **字型** ] 對話方塊，以取得使用者目前字型選取專案的相關資訊。


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，此結構會接收使用者目前字型選取範圍的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式會建立 [**字型**] 對話方塊。 當使用者關閉 [ **字型** ] 對話方塊時， **ChooseFont** 函式會傳回使用者在 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) 結構中選取之字型的相關資訊。 **CHOOSEFONT** 結構的 **LpLogFont** 成員是 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標。

在 [**字型**] 對話方塊開啟時，使用 **WM \_ CHOOSEFONT \_ GETLOGFONT** 訊息來取得使用者目前字型選取範圍的相關資訊。 例如，如果您啟用 [**字型**] 對話方塊中的 [套用 **] 按鈕，** 請傳送訊息以取得要套用至目前文字選取範圍的字型資訊。

一般來說，您會啟用 [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)攔截程式，以處理 **適用于**[套用] 按鈕的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息。 當使用者按一下 [套用 **] 按鈕時** ，攔截程式會將 **WM \_ CHOOSEFONT \_ GETLOGFONT** 訊息傳送至對話方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**WM \_ 命令**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

