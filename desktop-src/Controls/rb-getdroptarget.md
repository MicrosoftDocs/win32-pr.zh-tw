---
title: 'RB_GETDROPTARGET 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項的 IDropTarget 介面指標。
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5793d2192ef65f193ff27d40cc14660c90d067034d8c1304e1bde1a354a4f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169608"
---
# <a name="rb_getdroptarget-message"></a>RB \_ GETDROPTARGET 訊息

抓取 Rebar 控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 介面指標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget)指標的指標，該指標會接收介面指標。 當不再需要時，呼叫端會負責呼叫這個指標的 [**發行**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

