---
title: 'TVM_SETSCROLLTIME 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項的最大滾動時間。 您可以使用 TreeView SetScrollTime 宏明確地傳送此訊息 \_ 。
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- TVM_SETSCROLLTIME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c9ca3392de81a712aa6be7dc2addb87eedf65af4aa77958e5b7f5fbb2eafc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408485"
---
# <a name="tvm_setscrolltime-message"></a>TVM \_ SETSCROLLTIME 訊息

設定樹狀檢視控制項的最大滾動時間。 您可以使用 [**TreeView \_ SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

新的最大滾動時間（以毫秒為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回之前的最大滾動時間（以毫秒為單位）。

## <a name="remarks"></a>備註

最長的滾動時間是捲軸操作可花費的最長時間量。 將會調整滾動，讓捲軸在最大滾動時間內進行。 捲軸操作的時間可能會比最大值少。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ GETSCROLLTIME**](tvm-getscrolltime.md)
</dt> </dl>

 

 





