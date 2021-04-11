---
title: 'TVM_GETSCROLLTIME 訊息 (Commctrl .h) '
description: 抓取樹狀檢視控制項的最大滾動時間。 您可以使用 TreeView GetScrollTime 宏明確地傳送此訊息 \_ 。
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094159"
---
# <a name="tvm_getscrolltime-message"></a>TVM \_ GETSCROLLTIME 訊息

抓取樹狀檢視控制項的最大滾動時間。 您可以使用 [**TreeView \_ GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回最大滾動時間（以毫秒為單位）。

## <a name="remarks"></a>備註

最長的滾動時間是捲軸操作可花費的最長時間量。 將會調整滾動，讓捲軸在最大滾動時間內進行。 捲軸操作的時間可能會比最大值少。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETSCROLLTIME**](tvm-setscrolltime.md)
</dt> </dl>

 

 





