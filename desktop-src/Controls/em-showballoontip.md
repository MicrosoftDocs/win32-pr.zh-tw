---
title: 'EM_SHOWBALLOONTIP 訊息 (Commctrl .h) '
description: EM \_ SHOWBALLOONTIP 訊息會顯示與編輯控制項相關聯的氣球提示。
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- EM_SHOWBALLOONTIP message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104207"
---
# <a name="em_showballoontip-message"></a>EM \_ SHOWBALLOONTIP 訊息

**EM \_ SHOWBALLOONTIP** 訊息會顯示與編輯控制項相關聯的氣球提示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)結構的指標，其中包含要顯示之氣球提示的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則會傳回 **TRUE**。 否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[**編輯 \_ ShowBalloonTip**](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





