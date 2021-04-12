---
title: 'LVM_SUBITEMHITTEST 訊息 (Commctrl .h) '
description: 判斷哪一個清單視圖專案或子專案位於指定的位置。 您可以明確地傳送此訊息，或使用 ListView \_ SubItemHitTest 宏來傳送。
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST message Windows 控制項
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
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464408"
---
# <a name="lvm_subitemhittest-message"></a>LVM \_ SUBITEMHITTEST 訊息

判斷哪一個清單視圖專案或子專案位於指定的位置。 您可以明確地傳送此訊息，或使用 [**ListView \_ SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須是 0。 **Windows Vista。** 如果要取出 *lParam* 的 **iGroup** 成員，則應為-1。</dd> <dt>

*lParam* 
</dt> <dd>

[**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo)結構的指標。 **LVHITTESTINFO** 內的 [**點**](/previous-versions//dd162805(v=vs.85))結構應設定為要進行點擊測試的用戶端座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回已測試之專案或子專案的索引（如果有的話），否則為-1。 如果專案或子專案位於指定的座標， [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) 結構的欄位將會填入適用的點擊資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

