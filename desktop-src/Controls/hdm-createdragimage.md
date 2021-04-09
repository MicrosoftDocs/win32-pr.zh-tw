---
title: 'HDM_CREATEDRAGIMAGE 訊息 (Commctrl .h) '
description: 建立專案影像的半透明版本，作為拖曳影像使用。 您可以明確地傳送此訊息，或使用標頭 \_ CreateDragImage 宏。
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE message Windows 控制項
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
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025254"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





