---
title: 'LM_SETITEM 訊息 (Commctrl .h) '
description: 設定專案的狀態和屬性。
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- LM_SETITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dccdb37536352c8783f7dd6af6a9475f5bea69111e2f7f09e5395b0ebf25b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062798"
---
# <a name="lm_setitem-message"></a>LM \_ SETITEM 訊息

設定專案的狀態和屬性。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須是 **Null**。 </dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a>結構的指標，其中包含連結所需的新狀態和屬性。 </dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功設定指定的值和屬性，則傳回 **TRUE** 。

## <a name="remarks"></a>備註

使用 [**LM \_ GETITEM**](lm-getitem.md)訊息時，只能透過 [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem)的 **ashraf** 成員所傳回的數值索引來存取連結。 不支援透過 **szID** 中傳回的識別碼名稱來存取連結。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comctl32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





