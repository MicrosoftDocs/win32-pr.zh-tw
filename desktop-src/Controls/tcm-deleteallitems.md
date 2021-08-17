---
title: 'TCM_DELETEALLITEMS 訊息 (Commctrl .h) '
description: 從索引標籤控制項移除所有專案。 您可以使用 TabCtrl DeleteAllItems 宏明確地傳送此訊息 \_ 。
ms.assetid: 733494c4-38f4-44ba-98d2-c33a8d63c3b7
keywords:
- TCM_DELETEALLITEMS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a67a8e2fdf1137b51a1baf0097be3a555f404d13851a0e58fe301d3eafd5c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434148"
---
# <a name="tcm_deleteallitems-message"></a>TCM \_ DELETEALLITEMS 訊息

從索引標籤控制項移除所有專案。 您可以使用 [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





