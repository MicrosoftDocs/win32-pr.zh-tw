---
title: 'TVM_GETEDITCONTROL 訊息 (Commctrl .h) '
description: 抓取編輯控制項的控制碼，這個控制項是用來編輯樹狀檢視專案的文字。 您可以使用 TreeView GetEditControl 宏明確地傳送此訊息 \_ 。
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a591104085de793d8ea479656eb9100424ba5194a173fd93d10444c43e2cbfc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104428"
---
# <a name="tvm_geteditcontrol-message"></a>TVM \_ GETEDITCONTROL 訊息

抓取編輯控制項的控制碼，這個控制項是用來編輯樹狀檢視專案的文字。 您可以使用 [**TreeView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回編輯控制項的控制碼，否則傳回 **Null** 。

## <a name="remarks"></a>備註

當標籤編輯開始時，會建立編輯控制項，但不會定位或顯示。 在顯示之前，樹狀檢視控制項會將 [izdebski \_ BEGINLABELEDIT](tvn-beginlabeledit.md) 通知程式碼傳送給其父視窗。

若要自訂標籤編輯，請執行 [izdebski \_ BEGINLABELEDIT](tvn-beginlabeledit.md) 的處理常式，並讓它將 **TVM \_ GETEDITCONTROL** 訊息傳送至樹狀檢視控制項。 如果正在編輯標籤，傳回值將會是編輯控制項的控制碼。 您可以使用此控制碼來自訂編輯控制項，方法是傳送一般的 **EM \_ XXX** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





