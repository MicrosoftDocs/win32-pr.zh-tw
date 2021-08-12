---
title: 'TVM_SETITEMHEIGHT 訊息 (Commctrl .h) '
description: 設定樹狀檢視專案的高度。 您可以使用 TreeView SetItemHeight 宏明確地傳送此訊息 \_ 。
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afff57188a9683d18c6bff780b4a9f61479526d44ea77985742520a47e66cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669643"
---
# <a name="tvm_setitemheight-message"></a>TVM \_ SETITEMHEIGHT 訊息

設定樹狀檢視專案的高度。 您可以使用 [**TreeView \_ SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

樹狀檢視中每個專案的新高度（以圖元為單位）。 小於1的高度將設定為1。 如果這個引數不是偶數，而且樹狀檢視控制項沒有 [**tv \_ NONEVENHEIGHT**](tree-view-control-window-styles.md) 樣式，則這個值會向下舍入至最接近的偶數值。 如果這個引數是-1，控制項將會還原為使用其預設專案高度。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回專案的先前高度（以圖元為單位）。

## <a name="remarks"></a>備註

樹狀檢視控制項會使用此值作為所有專案的高度。 若要修改個別專案的高度，請參閱 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)結構之 **iIntegral** 成員的描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ GETITEMHEIGHT**](tvm-getitemheight.md)
</dt> </dl>

 

 





