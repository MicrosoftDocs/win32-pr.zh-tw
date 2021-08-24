---
title: 'TCM_GETITEM 訊息 (Commctrl .h) '
description: 抓取索引標籤控制項中索引標籤的相關資訊。 您可以使用 TabCtrl GetItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5403bb85e1b2747d1ab6081d33c25ec20a3b2099fc83b2b15e66b014f558584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876578"
---
# <a name="tcm_getitem-message"></a>TCM \_ GETITEM 訊息

抓取索引標籤控制項中索引標籤的相關資訊。 您可以使用 [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

索引標籤的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的指標，此結構會指定要取出的資訊，並接收索引標籤的相關資訊。傳送訊息時，**遮罩** 成員會指定要傳回的屬性。 如果 **遮罩** 成員指定 TCIF \_ 文字值， **pszText** 成員必須包含接收專案文字的緩衝區位址，而且 **cchTextMax** 成員必須指定緩衝區的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果在 \_ [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的 **MASK** 成員中設定 TCIF 文字旗標，控制項可能會變更結構的 **pszText** 成員以指向新的文字，而不是以要求的文字填滿緩衝區。 控制項可以將 **pszText** 成員設為 **Null** ，表示沒有任何文字與專案相關聯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TCM \_GETITEMW** (Unicode) 和 **TCM \_ GETITEMA** (ANSI) <br/>                   |



 

 





