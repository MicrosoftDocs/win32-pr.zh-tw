---
title: 'LVM_GETFOOTERITEM 訊息 (Commctrl .h) '
description: 取得清單視圖控制項中頁尾專案的資訊。 明確地傳送此訊息，或使用 ListView \_ GetFooterItem 宏。
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024588"
---
# <a name="lvm_getfooteritem-message"></a>LVM \_ GETFOOTERITEM 訊息

取得清單視圖控制項中頁尾專案的資訊。 明確地傳送此訊息，或使用 [**ListView \_ GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

項目的索引。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

[**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem)結構的指標，可根據 **mask** 成員的值接收 **狀態** 和/或 **pszText** 成員的值。 呼叫進程負責配置此結構並設定其成員，向接收者指出要傳回的資訊。 如需詳細資訊，請參閱 **LVFOOTERITEM**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





