---
title: 'DTM_GETSYSTEMTIME 訊息 (Commctrl .h) '
description: 從日期和時間選擇器取得目前選取的時間 (DTP) 控制項，並將它放在指定的 SYSTEMTIME 結構中。 您可以明確地傳送此訊息，或使用 DateTime \_ GetSystemtime 宏。
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- DTM_GETSYSTEMTIME message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104843"
---
# <a name="dtm_getsystemtime-message"></a>DTM \_ GETSYSTEMTIME 訊息

從日期和時間選擇器取得目前選取的時間 (DTP) 控制項，並將它放在指定的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構中。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標。 如果 **DTM \_ GETSYSTEMTIME** 傳回 GDT \_ VALID，此結構將會包含目前所選取的時間。 否則，它不會包含有效的資訊。 此參數必須是有效的指標;它不能是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功將時間資訊放入 *lParam* 中，則傳回 GDT 有效。 \_如果控制項設定為 [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md)樣式，而且沒有選取控制項核取方塊，則會傳回 GDT NONE。 \_如果發生錯誤，則傳回 GDT 錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

