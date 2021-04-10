---
title: 'TVM_GETITEMHEIGHT 訊息 (Commctrl .h) '
description: 抓取每個樹狀檢視專案目前的高度。 您可以使用 TreeView GetItemHeight 宏明確地傳送此訊息 \_ 。
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- TVM_GETITEMHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844435"
---
# <a name="tvm_getitemheight-message"></a>TVM \_ GETITEMHEIGHT 訊息

抓取每個樹狀檢視專案目前的高度。 您可以使用 [**TreeView \_ GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回每個專案的高度（以圖元為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETITEMHEIGHT**](tvm-setitemheight.md)
</dt> </dl>

 

 





