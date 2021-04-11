---
title: 'TVM_GETINDENT 訊息 (Commctrl .h) '
description: 以圖元為單位，抓取子專案相對於其父代專案的縮排量（以圖元為單位）。 您可以使用 TreeView setindent 宏明確地傳送此訊息 \_ 。
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844251"
---
# <a name="tvm_getindent-message"></a>TVM \_ setindent 訊息

以圖元為單位，抓取子專案相對於其父代專案的縮排量（以圖元為單位）。 您可以使用 [**TreeView \_ setindent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回縮排的量。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





