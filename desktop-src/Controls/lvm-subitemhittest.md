---
title: 'LVM_SUBITEMHITTEST 訊息 (Commctrl .h) '
description: 判斷哪一個清單視圖專案或子專案位於指定的位置。 您可以明確地傳送此訊息，或使用 ListView \_ SubItemHitTest 宏來傳送。
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341f9b3f84646abe975c6543aef802450496154862353b7bbdd1af2c07c087ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830639"
---
# <a name="lvm_subitemhittest-message"></a>LVM \_ SUBITEMHITTEST 訊息

判斷哪一個清單視圖專案或子專案位於指定的位置。 您可以明確地傳送此訊息，或使用 [**ListView \_ SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須是 0。 **WindowsVista。** 如果要取出 *lParam* 的 **iGroup** 成員，則應為-1。</dd> <dt>

*lParam* 
</dt> <dd>

[**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo)結構的指標。 **LVHITTESTINFO** 內的 [**點**](/previous-versions//dd162805(v=vs.85))結構應設定為要進行點擊測試的用戶端座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回已測試之專案或子專案的索引（如果有的話），否則為-1。 如果專案或子專案位於指定的座標， [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) 結構的欄位將會填入適用的點擊資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

