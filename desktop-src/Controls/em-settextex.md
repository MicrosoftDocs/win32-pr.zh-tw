---
title: 'EM_SETTEXTEX 訊息 (Richedit .h) '
description: 結合了 WM \_ SETTEXT 和 EM \_ REPLACESEL 訊息的功能，並新增使用字碼頁設定文字的功能，以及使用 rtf 或純文字。
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- EM_SETTEXTEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465704"
---
# <a name="em_settextex-message"></a>EM \_ SETTEXTEX 訊息

結合了 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 和 [**EM \_ REPLACESEL**](em-replacesel.md) 訊息的功能，並新增使用字碼頁設定文字的功能，以及使用 rtf 或純文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)結構的指標，此結構會指定旗標以及要用於翻譯為 Unicode 的選擇性字碼頁。

</dd> <dt>

*lParam* 
</dt> <dd>

要插入之以 null 結束的文字指標。 除非字碼頁是 1200 (Unicode) ，否則此文字為 ANSI 字串。 如果 *lParam* 以有效的 rtf ASCII 序列（例如 "{ \\ RTF" 或 "{urtf"）開頭，則會使用 RTF 讀取器來讀取文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業正在設定所有文字且成功，則傳回值為1。

如果作業正在設定選取範圍，且成功，則傳回值為複製的位元組數或字元數。

如果作業失敗，則傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETTEXTEX**](em-gettextex.md)
</dt> <dt>

[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

