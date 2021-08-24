---
title: 'TVM_ENSUREVISIBLE 訊息 (Commctrl .h) '
description: 確定樹狀檢視專案可見、展開父專案或滾動樹狀檢視控制項（如有必要）。 您可以使用 TreeView EnsureVisible 宏明確地傳送此訊息 \_ 。
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1072c7213eb2172896980662bcd7a22a3c41fccf34eea2f7a107ab7ff894b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797248"
---
# <a name="tvm_ensurevisible-message"></a>TVM \_ ENSUREVISIBLE 訊息

確定樹狀檢視專案可見、展開父專案或滾動樹狀檢視控制項（如有必要）。 您可以使用 [**TreeView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

專案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果系統滾動樹狀檢視控制項中的專案，但未展開任何專案，則傳回非零。 否則，訊息會傳回零。

## <a name="remarks"></a>備註

如果 TVM \_ ENSUREVISIBLE 訊息展開父項目，父視窗會接收 [izdebski \_ ITEMEXPANDING](tvn-itemexpanding.md) 和 [izdebski \_ ITEMEXPANDED](tvn-itemexpanded.md) 通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





