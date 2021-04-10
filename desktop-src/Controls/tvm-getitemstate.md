---
title: 'TVM_GETITEMSTATE 訊息 (Commctrl .h) '
description: 抓取部分或所有樹狀檢視專案的狀態屬性。 您可以使用 TreeView GetItemState 宏明確地傳送此訊息 \_ 。
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025276"
---
# <a name="tvm_getitemstate-message"></a>TVM \_ GETITEMSTATE 訊息

抓取部分或所有樹狀檢視專案的狀態屬性。 您可以使用 [**TreeView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

專案的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

用來指定要查詢之狀態的遮罩。 它相當於 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)的 **stateMask** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回將適當的狀態位設為 **TRUE** 的 **UINT** 值。 只有 *lParam* 指定且為 **TRUE** 的位會進行設定。 此值相當於 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)的 **狀態** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





