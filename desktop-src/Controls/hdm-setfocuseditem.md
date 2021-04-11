---
title: 'HDM_SETFOCUSEDITEM 訊息 (Commctrl .h) '
description: 將焦點設定為標題控制項中的指定專案。 明確地傳送此訊息，或使用標頭 \_ SetFocusedItem 宏。
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- HDM_SETFOCUSEDITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105293"
---
# <a name="hdm_setfocuseditem-message"></a>HDM \_ SETFOCUSEDITEM 訊息

將焦點設定為標題控制項中的指定專案。 明確地傳送此訊息，或使用 [**標頭 \_ SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>未使用。 必須為零。</dd> <dt>

*lParam* \[在\]
</dt> <dd>

專案的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於標題控制項](header-controls.md)
</dt> </dl>

 

 





