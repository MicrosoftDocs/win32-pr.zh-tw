---
title: 'TCM_REMOVEIMAGE 訊息 (Commctrl .h) '
description: 從索引標籤控制項的影像清單中移除影像。 您可以使用 TabCtrl RemoveImage 宏明確地傳送此訊息 \_ 。
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- TCM_REMOVEIMAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d2305386f948e1dc4522124708b31ca360203ba9723241c99262fcdb5d2b20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104838"
---
# <a name="tcm_removeimage-message"></a>TCM \_ REMOVEIMAGE 訊息

從索引標籤控制項的影像清單中移除影像。 您可以使用 [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要移除之映射的索引。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

索引標籤控制項會更新每個索引標籤的影像索引，因此每個索引標籤都會與之前的映射保持相關聯。 如果索引標籤使用正在移除的影像，索引標籤將設定為沒有影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





