---
title: 'EM_SETWORDBREAKPROC 訊息 (Winuser .h) '
description: 使用應用程式定義的 Wordwrap 函數來取代編輯控制項的預設 Wordwrap 函式。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508707"
---
# <a name="em_setwordbreakproc-message"></a>EM \_ SETWORDBREAKPROC 訊息

使用應用程式定義的 Wordwrap 函數來取代編輯控制項的預設 Wordwrap 函式。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

應用程式定義的 Wordwrap 函式的位址。 如需有關中斷線的詳細資訊，請參閱 [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) 回呼函式的描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

Wordwrap 函式會掃描文字緩衝區，其中包含要傳送至螢幕的文字，並尋找不符合目前畫面線的第一個字組。 Wordwrap 函式會將這個單字放在畫面上下一行的開頭。

Wordwrap 函式會定義系統應該將多行編輯控制項的文字換行的點，通常是在分隔兩個單字的空白字元上。 當使用者按下方向鍵和 CTRL 鍵，以將插入號移到下一個單字或上一個字組時，多行或單行編輯控制項可能會呼叫此函式。 預設的 Wordwrap 函式會在空白字元上中斷一行文字。 應用程式定義函式可能會定義要在連字號或空白字元以外的字元上發生的 Wordwrap。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**EM \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**EM \_ GETWORDBREAKPROC**](em-getwordbreakproc.md)
</dt> </dl>

 

