---
title: 'DTM_CLOSEMONTHCAL 訊息 (Commctrl .h) '
description: 關閉 (DTP) 控制項的日期和時間選擇器。 請明確地傳送此訊息，或使用 DateTime \_ CloseMonthCal 宏。
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024674"
---
# <a name="dtm_closemonthcal-message"></a>DTM \_ CLOSEMONTHCAL 訊息

關閉 (DTP) 控制項的日期和時間選擇器。 請明確地傳送此訊息，或使用 [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零。

## <a name="remarks"></a>備註

終結控制項，並傳送控制項正在關閉的 [DTN \_ 特寫](dtn-closeup.md) 通知，而不是控制項開啟 (下拉式清單，如同在控制項的父系) 的 [DTN \_ 下拉式](dtn-dropdown.md) 通知中一樣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[DTN \_ 下拉式清單](dtn-dropdown.md)
</dt> <dt>

[DTN \_ 特寫](dtn-closeup.md)
</dt> </dl>

 

 





