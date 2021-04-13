---
title: 'RB_BEGINDRAG 訊息 (Commctrl .h) '
description: 將 Rebar 控制項放在拖放模式中。 此訊息不會造成 RBN \_ BEGINDRAG 通知傳送。
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- RB_BEGINDRAG message Windows 控制項
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466089"
---
# <a name="rb_begindrag-message"></a>RB \_ BEGINDRAG 訊息

將 Rebar 控制項放在拖放模式中。 此訊息不會造成 [RBN \_ BEGINDRAG](rbn-begindrag.md) 通知傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，此為拖放作業會影響的頻外索引。

</dd> <dt>

*lParam* 
</dt> <dd>

包含開始滑鼠座標的 **DWORD** 值。 水準座標是包含在 LOWORD 中，而垂直座標則是包含在 HIWORD 中。 如果您傳遞 (**DWORD**) -1，Rebar 控制項將會使用滑鼠的位置，這是上一次控制項的執行緒，稱為 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

**Rb \_ BEGINDRAG**、 [**rb \_ DRAGMOVE**](rb-dragmove.md)和 [**rb \_ ENDDRAG**](rb-enddrag.md)訊息可讓您針對 Rebar 控制項執行 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget)介面。 您會傳送 **rb \_ BEGINDRAG** 訊息以回應 [**IDropTarget：:D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter)、傳送 **rb \_ DRAGMOVE** 訊息以回應 [**IDropTarget：:D Ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)，並傳送 **rb \_ ENDDRAG** 訊息以回應 [**IDropTarget：:D rop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) 和 [**IDropTarget：:D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

