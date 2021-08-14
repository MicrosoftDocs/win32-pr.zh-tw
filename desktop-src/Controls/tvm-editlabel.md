---
title: 'TVM_EDITLABEL 訊息 (Commctrl .h) '
description: 開始編輯指定專案的文字，並將專案的文字取代為包含文字的單行編輯控制項。
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ba9f9d0af4d6afb3c454f5e5477ccd67728bdec7f378b0f0a04adc901ba322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408585"
---
# <a name="tvm_editlabel-message"></a>TVM \_ EDITLABEL 訊息

開始編輯指定專案的文字，並將專案的文字取代為包含文字的單行編輯控制項。 此訊息會隱含地選取並將焦點放在指定的專案。 您可以使用 [**TreeView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

要編輯之專案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回編輯控制項所用的編輯控制項的控制碼，否則傳回 **Null** 。

## <a name="remarks"></a>備註

此訊息會將 [izdebski \_ BEGINLABELEDIT](tvn-beginlabeledit.md) 通知程式碼傳送至樹狀檢視控制項的父代。

當使用者完成或取消編輯時，就會終結編輯控制項，而且控制碼不再有效。 您可以子類別化編輯控制項，但不要終結它。

當您將此訊息傳送至控制項之前，控制項必須具有焦點。 您可以使用 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數來設定焦點。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TVM \_EDITLABELW** (Unicode) 和 **TVM \_ EDITLABELA** (ANSI) <br/>               |



 

