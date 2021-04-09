---
title: 'MCM_SETSELRANGE 訊息 (Commctrl .h) '
description: 將月曆控制項的選取範圍設定為指定的日期範圍。 您可以使用 MonthCal SetSelRange 宏明確地傳送此訊息 \_ 。
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- MCM_SETSELRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024657"
---
# <a name="mcm_setselrange-message"></a>MCM \_ SETSELRANGE 訊息

將月曆控制項的選取範圍設定為指定的日期範圍。 您可以使用 [**MonthCal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標，其中包含代表選取限制的日期資訊。 第一個選取的日期必須指定于 *lpSysTimeArray* \[ 0 \] ，而且必須在 *lpSysTimeArray* 1 中指定最後選取的日期 \[ \] 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。 如果套用到不使用 [**MCS \_ 多重選**](month-calendar-control-styles.md) 樣式的月曆控制項，此訊息將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[月曆控制項中的時間](month-calendar-controls.md)
</dt> </dl>

 

