---
title: 'TCM_SETCURSEL 訊息 (Commctrl .h) '
description: 在索引標籤控制項中選取索引標籤。 您可以使用 TabCtrl SetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934404"
---
# <a name="tcm_setcursel-message"></a>TCM \_ SETCURSEL 訊息

在索引標籤控制項中選取索引標籤。 您可以使用 [**TabCtrl \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要選取之索引標籤的索引。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回先前所選索引標籤的索引，否則傳回-1。

## <a name="remarks"></a>備註

使用此訊息選取索引標籤時，不會傳送 [TCN \_ SELCHANGING](tcn-selchanging.md) 或 [TCN \_ SELCHANGE](tcn-selchange.md) 通知碼給索引標籤控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





