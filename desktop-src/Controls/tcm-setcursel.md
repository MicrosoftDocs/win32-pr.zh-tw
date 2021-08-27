---
title: 'TCM_SETCURSEL 訊息 (Commctrl .h) '
description: 在索引標籤控制項中選取索引標籤。 您可以使用 TabCtrl SetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- TCM_SETCURSEL 訊息 Windows 控制項
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
ms.openlocfilehash: 5bdfd0861f5249a823d9406b437fd0efbca64a757a4bcadd7991155a87ddbc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104848"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





