---
title: 'TCM_SETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 設定索引標籤控制項將使用的擴充樣式。 您可以使用 TabCtrl SetExtendedStyle 宏明確地傳送此訊息 \_ 。
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- TCM_SETEXTENDEDSTYLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a28bcf4cffe9aa2559f96a990d23511ece9fbbfc65468f84a4a874dce678a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876448"
---
# <a name="tcm_setextendedstyle-message"></a>TCM \_ SETEXTENDEDSTYLE 訊息

設定索引標籤控制項將使用的擴充樣式。 您可以使用 [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** 值，指出要對 *lParam* 中的哪些樣式造成影響。 只有 *wParam* 中的擴充樣式會變更。 所有其他樣式都會維持不變。 如果此參數為零，則 *lParam* 中的所有樣式都會受到影響。

</dd> <dt>

*lParam* 
</dt> <dd>

指定擴充的索引標籤控制項樣式的值。 此值為索引標籤控制項 [擴充樣式](tab-control-extended-styles.md)的組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含先前的索引標籤控制項擴充樣式的 **DWORD** 值。

## <a name="remarks"></a>備註

*WParam* 參數可讓您修改一或多個擴充樣式，而不需要先取出現有的樣式。 例如，如果您傳遞 [**TCS 的 \_ \_ FLATSEPARATORS**](tab-control-extended-styles.md) for *wParam* 和0（ *lParam*），將會清除 **TCS \_ EX \_ FLATSEPARATORS** 樣式，但所有其他樣式都會保持不變。

基於回溯相容性的理由， [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) 宏尚未更新為使用 *dwExMask*。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





