---
title: 'HDM_CREATEDRAGIMAGE 訊息 (Commctrl .h) '
description: 建立專案影像的半透明版本，作為拖曳影像使用。 您可以明確地傳送此訊息，或使用標頭 \_ CreateDragImage 宏。
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1507f3e72ce75394aaad834fe5c0d876fc579a671ad8f2df00865b2278ad6e32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047228"
---
# <a name="hdm_createdragimage-message"></a>HDM \_ CREATEDRAGIMAGE 訊息

建立專案影像的半透明版本，作為拖曳影像使用。 您可以明確地傳送此訊息，或使用 [**標頭 \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

標題控制項中專案的以零為基底的索引。 指派給此專案的影像是透明影像的基礎。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回影像清單的控制碼，其中包含新的影像做為其唯一的元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





