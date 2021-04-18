---
title: 'EM_GETWORDBREAKPROC 訊息 (Winuser .h) '
description: 取得目前 Wordwrap 函式的位址。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466236"
---
# <a name="em_getwordbreakproc-message"></a>EM \_ GETWORDBREAKPROC 訊息

取得目前 Wordwrap 函式的位址。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會指定應用程式定義的 Wordwrap 函式的位址。 如果沒有任何 Wordwrap 函數，則傳回值為 **Null** 。

## <a name="remarks"></a>備註

Wordwrap 函式會掃描包含要傳送給顯示之文字的文字緩衝區，尋找不符合目前顯示行的第一個單字。 Wordwrap 函式會將這個單字放在顯示器上下一行的開頭。 Wordwrap 函式會定義系統應該將多行編輯控制項的文字換行的點，通常是在分隔兩個單字的空白字元上。

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

[**EM \_ SETWORDBREAKPROC**](em-setwordbreakproc.md)
</dt> </dl>

 

