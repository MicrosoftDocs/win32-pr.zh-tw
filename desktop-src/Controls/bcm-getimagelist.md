---
title: 'BCM_GETIMAGELIST 訊息 (Commctrl .h) '
description: 取得按鈕 \_ IMAGELIST 結構，描述指派給按鈕控制項的影像清單。 您可以明確地傳送此訊息，或使用按鈕 \_ GetImageList 宏。
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- BCM_GETIMAGELIST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba74f358e80871ffad4822fd8088ca6aeb58521d8878254ed920356db5a6daf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833909"
---
# <a name="bcm_getimagelist-message"></a>BCM \_ GETIMAGELIST 訊息

取得 [**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) 結構，描述指派給按鈕控制項的影像清單。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist)結構的指標，其中包含影像清單資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則會傳回 **TRUE**。 否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





