---
title: 'TVM_GETINDENT 訊息 (Commctrl .h) '
description: 以圖元為單位，抓取子專案相對於其父代專案的縮排量（以圖元為單位）。 您可以使用 TreeView setindent 宏明確地傳送此訊息 \_ 。
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT 訊息 Windows 控制項
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
ms.openlocfilehash: bbee65da49efc19954209b2694d783761017d8c2ae53030e755b8bea61213276
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834178"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





