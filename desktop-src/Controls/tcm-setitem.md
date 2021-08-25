---
title: 'TCM_SETITEM 訊息 (Commctrl .h) '
description: 設定部分或全部索引標籤的屬性。 您可以使用 TabCtrl SetItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27f93e2743e5676c0fcca932cfa1936bb72667ef4fa4a5334eaae3e78d2be08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876321"
---
# <a name="tcm_setitem-message"></a>TCM \_ SETITEM 訊息

設定部分或全部索引標籤的屬性。 您可以使用 [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的指標，其中包含新的專案屬性。 **遮罩** 成員會指定要設定的屬性。 如果 **遮罩** 成員指定 TCIF \_ 文字值，則 **pszText** 成員是以 null 結束之字串的位址，而且會忽略 **cchTextMax** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TCM \_SETITEMW** (Unicode) 和 **TCM \_ SETITEMA** (ANSI) <br/>                   |



 

 





