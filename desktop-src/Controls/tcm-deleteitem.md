---
title: 'TCM_DELETEITEM 訊息 (Commctrl .h) '
description: 從索引標籤控制項移除專案。 您可以使用 TabCtrl DeleteItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934950"
---
# <a name="tcm_deleteitem-message"></a>TCM \_ DELETEITEM 訊息

從索引標籤控制項移除專案。 您可以使用 [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要刪除之專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





