---
title: 'LVM_EDITLABEL 訊息 (Commctrl .h) '
description: 開始就地編輯指定清單視圖專案的文字。 訊息會隱含地選取並將焦點放在指定的專案。 您可以明確地傳送此訊息，或使用 ListView \_ EditLabel 宏來傳送。
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be1896c39e06c25bf06e033d74a17107b3e194a43b1c574e1dcb7f9a456413
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411842"
---
# <a name="lvm_editlabel-message"></a>LVM \_ EDITLABEL 訊息

開始就地編輯指定清單視圖專案的文字。 訊息會隱含地選取並將焦點放在指定的專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖專案的索引。 若要取消編輯，請將索引設定為-1。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回編輯控制項的控制碼，如果成功，則會用來編輯專案文字，否則傳回 **Null** 。

## <a name="remarks"></a>備註

當使用者完成或取消編輯時，就會終結編輯控制項，而且控制碼不再有效。 您可以子類別化編輯控制項，但您不應該將它終結。

當您將此訊息傳送至控制項之前，控制項必須具有焦點。 您可以使用 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數來設定焦點。

如果 *wParam* 為-1，則會傳送 [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) 通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_EDITLABELW** (Unicode) 和 **LVM \_ EDITLABELA** (ANSI) <br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

