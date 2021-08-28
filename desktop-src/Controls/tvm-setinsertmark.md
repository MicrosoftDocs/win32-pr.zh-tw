---
title: 'TVM_SETINSERTMARK 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項中的插入標記。 您可以使用 TreeView SetInsertMark 宏明確地傳送此訊息 \_ 。
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- TVM_SETINSERTMARK 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c3004395dcc7ea0b83af2fc2b7dae370c303228f79599215d5b6d264379b793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875628"
---
# <a name="tvm_setinsertmark-message"></a>TVM \_ SETINSERTMARK 訊息

設定樹狀檢視控制項中的插入標記。 您可以使用 [**TreeView \_ SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**布林** 值，指定插入標記是放置在指定的專案之前或之後。 如果這個引數不是零，則插入標記將放置在專案之後。 如果這個引數為零，則會在專案之前放置插入標記。

</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** ，指定將放置插入標記的專案。 如果這個引數為 **Null**，則會移除插入標記。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

在某些情況下，插入標記可以出現在節點展開之後的兩個位置中。 如果您使用插入標記，建議您在展開節點之後強制重新整理控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





