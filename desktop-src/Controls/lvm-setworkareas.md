---
title: 'LVM_SETWORKAREAS 訊息 (Commctrl .h) '
description: 設定清單視圖控制項內的工作區域。 您可以明確地傳送此訊息，或使用 ListView \_ SetWorkAreas 宏。
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934887"
---
# <a name="lvm_setworkareas-message"></a>LVM \_ SETWORKAREAS 訊息

設定清單視圖控制項內的工作區域。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

陣列中 *lprc* 的結構數目。 允許的工作區域數目上限是由 LV \_ MAX \_ WORKAREAS 值定義。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構陣列的指標，其中包含清單視圖控制項的新工作區域。 這些結構中的值是在用戶端座標中。 如果這個參數為 **Null**，工作區將會設定為控制項的工作區。 *wParam* 指定此陣列中的結構數目。

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

 

