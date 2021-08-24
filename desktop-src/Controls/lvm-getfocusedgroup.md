---
title: 'LVM_GETFOCUSEDGROUP 訊息 (Commctrl .h) '
description: 取得具有焦點的群組。 明確地傳送此訊息，或使用 ListView \_ GetFocusedGroup 宏。
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9b253405683c058518706e92e62f09041ae4db0e4bee426aa653103bda2188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877428"
---
# <a name="lvm_getfocusedgroup-message"></a>LVM \_ GETFOCUSEDGROUP 訊息

取得具有焦點的群組。 明確地傳送此訊息，或使用 [**ListView \_ GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回狀態為 LVGS 之群組的索引 \_ ，如果沒有焦點在 LVGS 狀態的群組，則為-1 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





