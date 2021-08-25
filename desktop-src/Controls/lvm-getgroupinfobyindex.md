---
title: 'LVM_GETGROUPINFOBYINDEX 訊息 (Commctrl .h) '
description: 取得指定群組的資訊。 明確地傳送此訊息，或使用 ListView \_ GetGroupInfoByIndex 宏。
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482683e9d1026c1deed17bf1f05310d63ac2127a6a2a6f32b5b5d95a0fbbea3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877398"
---
# <a name="lvm_getgroupinfobyindex-message"></a>LVM \_ GETGROUPINFOBYINDEX 訊息

取得指定群組的資訊。 明確地傳送此訊息，或使用 [**ListView \_ GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

群組的索引。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

[**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)結構的指標，用來接收 *wParam* 所指定之群組的資訊。 呼叫進程負責為結構和結構中的任何緩衝區（例如 **pszHeader** 成員所指向的緩衝區）配置記憶體。 設定結構的任何有的成員，例如 **CchHeader** **pszHeader** 在 **WCHARs** 中所指向的緩衝區大小，包括終止的 **Null**。 將 **cbSize** 設定為 SIZEOF (LVGROUP) 。

訊息接收者負責為結構成員設定 *wParam* 所指定之群組的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





