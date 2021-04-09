---
title: 'LVM_REDRAWITEMS 訊息 (Commctrl .h) '
description: 強制清單視圖控制項重新繪製某個範圍的專案。 您可以明確地傳送此訊息，或使用 ListView \_ RedrawItems 宏來傳送。
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025077"
---
# <a name="lvm_redrawitems-message"></a>LVM \_ REDRAWITEMS 訊息

強制清單視圖控制項重新繪製某個範圍的專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要重繪之第一個專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

要重繪之最後一個專案的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

在清單視圖視窗收到要重新繪製的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息之前，不會實際重新繪製指定的專案。 若要立即重新繪製，請在使用這個宏之後呼叫 [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

