---
title: 'DTM_GETMONTHCAL 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器的 (DTP) 子月曆控制項的控制碼。 您可以明確地傳送此訊息，或使用 DateTime \_ GetMonthCal 宏。
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- DTM_GETMONTHCAL message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934739"
---
# <a name="dtm_getmonthcal-message"></a>DTM \_ GETMONTHCAL 訊息

取得日期和時間選擇器的 (DTP) 子月曆控制項的控制碼。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會將控制碼傳回給 DTP 控制項的子月曆控制項，否則會傳回 **Null** 。

## <a name="remarks"></a>備註

當使用者按一下下拉式箭號 ([DTN \_ ](dtn-dropdown.md) 下拉式通知) 時，會建立一個子月曆控制項。 當月曆不再需要時，它會被終結 (在) 上傳送 [DTN 的 \_ 特寫](dtn-closeup.md) 通知。 因此，您的應用程式不得依賴 DTP 控制項之子月份行事曆的靜態控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[DTN \_ 特寫](dtn-closeup.md)
</dt> <dt>

[DTN \_ 下拉式清單](dtn-dropdown.md)
</dt> </dl>

 

 





