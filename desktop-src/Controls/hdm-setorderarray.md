---
title: 'HDM_SETORDERARRAY 訊息 (Commctrl .h) '
description: 設定標頭專案的由左到右順序。 您可以明確地傳送此訊息，或使用標頭 \_ SetOrderArray 宏。
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- HDM_SETORDERARRAY message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465480"
---
# <a name="hdm_setorderarray-message"></a>HDM \_ SETORDERARRAY 訊息

設定標頭專案的由左到右順序。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*LParam* 中的緩衝區大小（以元素為限）。 此值必須等於 [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)所傳回的值。

</dd> <dt>

*lParam* 
</dt> <dd>

陣列的指標，這個陣列會指定專案的顯示順序（從左至右）。 例如，如果陣列的內容是 {2,0,1} ，控制項會從左至右顯示專案2、專案0和專案1。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





