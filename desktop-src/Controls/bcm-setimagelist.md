---
title: 'BCM_SETIMAGELIST 訊息 (Commctrl .h) '
description: 將影像清單指派給按鈕控制項。 您可以明確地傳送此訊息，或使用按鈕 \_ SetImageList 宏。
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5c88020bb139c358b17386b003bfb9de9cfcd4e769b9262ed90e23f3f95e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921558"
---
# <a name="bcm_setimagelist-message"></a>BCM \_ SETIMAGELIST 訊息

將影像清單指派給按鈕控制項。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) 宏。

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

 

[**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist)結構的 **himl** 成員中所參考的影像清單，應包含要用於所有狀態的單一影像，或每個狀態的個別影像。 下列是在 vssym32 中定義的狀態。

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

請注意，PBS \_ STYLUSHOT 只會用於 tablet 電腦。

每個值都是影像清單中適當影像的索引。 如果只有一個映射存在，則會用於所有狀態。 如果影像清單包含一個以上的影像，每個索引都會對應至按鈕的一個狀態。 如果未針對每個狀態提供映射，則不會針對沒有影像的狀態繪製任何專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





