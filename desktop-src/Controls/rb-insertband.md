---
title: 'RB_INSERTBAND 訊息 (Commctrl .h) '
description: 在 Rebar 控制項中插入新的波段。
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- RB_INSERTBAND message Windows 控制項
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844456"
---
# <a name="rb_insertband-message"></a>RB \_ INSERTBAND 訊息

在 Rebar 控制項中插入新的波段。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，也就是要插入頻外的位置。 如果您將此參數設定為-1，此控制項將會在最後一個位置新增新的頻外。

</dd> <dt>

*lParam* 
</dt> <dd>

[**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的指標，該結構定義要插入的帶狀。 在傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **sizeof** (REBARBANDINFO) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **RB \_INSERTBANDW** (Unicode) 和 **RB \_ INSERTBANDA** (ANSI) <br/>               |



 

 





