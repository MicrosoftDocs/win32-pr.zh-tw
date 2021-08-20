---
title: 'PGM_SETCHILD 訊息 (Commctrl .h) '
description: 設定呼機控制項的包含視窗。
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da3424eabfb87d587ac8cd33802dfc03b3c3868d881b131360bfee2e8bc26730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830169"
---
# <a name="pgm_setchild-message"></a>PGM \_ SETCHILD 訊息

設定呼機控制項的包含視窗。 此訊息不會變更包含視窗的父系;它只會將視窗控制碼指派給呼機控制項以供滾動。 在大部分的情況下，包含的視窗將會是子視窗。 如果是這種情況，則包含的視窗應該是呼機控制項的子系。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

要包含的視窗控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





