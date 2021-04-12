---
title: 'TB_GETSTRING 訊息 (Commctrl .h) '
description: 從工具列的字串集區抓取字串。
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- TB_GETSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024853"
---
# <a name="tb_getstring-message"></a>TB \_ GETSTRING 訊息

從工具列的字串集區抓取字串。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定 *lParam* 緩衝區的長度（以位元組為單位）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定字串的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

用來傳回字串的緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回字串長度，否則傳回-1。

## <a name="remarks"></a>備註

此訊息會從工具列的字串集區傳回指定的字串。 它不一定會對應到目前由按鈕所顯示的文字字串。 若要抓取按鈕的目前文字字串，請將該工具列傳送至 [**TB 的 \_ GETBUTTONTEXT**](tb-getbuttontext.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_GETSTRINGW** (Unicode) 和 **TB \_ GETSTRINGA** (ANSI) <br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TB \_ ADDSTRING**](tb-addstring.md)
</dt> <dt>

[**TB \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

