---
title: 'HDM_GETFOCUSEDITEM 訊息 (Commctrl .h) '
description: 取得標題控制項中具有焦點的專案。 明確地傳送此訊息，或使用標頭 \_ GetFocusedItem 宏。
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- HDM_GETFOCUSEDITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465888"
---
# <a name="hdm_getfocuseditem-message"></a>HDM \_ GETFOCUSEDITEM 訊息

取得標題控制項中具有焦點的專案。 明確地傳送此訊息，或使用 [**標頭 \_ GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>未使用。 必須為零。</dd> <dt>

*lParam* 
</dt> <dd>未使用。 必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回焦點專案的索引。

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

 

 





