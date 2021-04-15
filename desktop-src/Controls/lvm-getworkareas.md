---
title: 'LVM_GETWORKAREAS 訊息 (Commctrl .h) '
description: 從清單視圖控制項抓取工作區域。 您可以明確地傳送此訊息，或使用 ListView \_ GetWorkAreas 宏。
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466500"
---
# <a name="lvm_getworkareas-message"></a>LVM \_ GETWORKAREAS 訊息

從清單視圖控制項抓取工作區域。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

陣列中 *lParam* 的 [**RECT**](/previous-versions//dd162897(v=vs.85))結構數目。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))陣列的指標，此陣列會接收清單視圖控制項目前的工作區域。 這些結構中的值是在用戶端座標中。 *wParam* 指定此陣列中的結構數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 List-View 控制項](using-list-view-controls.md)
</dt> </dl>

 

