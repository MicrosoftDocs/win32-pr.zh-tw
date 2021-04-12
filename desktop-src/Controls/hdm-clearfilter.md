---
title: 'HDM_CLEARFILTER 訊息 (Commctrl .h) '
description: 清除指定標題控制項的篩選。 您可以明確地傳送此訊息，或使用標頭 \_ ClearFilter 宏。
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- HDM_CLEARFILTER message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104490"
---
# <a name="hdm_clearfilter-message"></a>HDM \_ CLEARFILTER 訊息

清除指定標題控制項的篩選。 您可以明確地傳送此訊息，或使用 [**標頭 \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出要清除之篩選準則的資料行值。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數。 **LRESULT** 會轉換為整數，表示 **TRUE** (1) 或 **FALSE** (0) 。

## <a name="remarks"></a>備註

如果將資料行值指定為-1，則會清除所有篩選，而 [HDN \_ FILTERCHANGE](hdn-filterchange.md) 通知只會傳送一次。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**標頭 \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





