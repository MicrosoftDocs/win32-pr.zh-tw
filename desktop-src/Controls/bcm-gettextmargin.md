---
title: 'BCM_GETTEXTMARGIN 訊息 (Commctrl .h) '
description: 取得用來在按鈕控制項中繪製文字的邊界。 您可以明確地傳送此訊息，或使用按鈕 \_ GetTextMargin 宏。
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- BCM_GETTEXTMARGIN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea871d0054558e1522011d4fdb00fdd3c82a0dd1562fe3420d3295bbab89a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064408"
---
# <a name="bcm_gettextmargin-message"></a>BCM \_ GETTEXTMARGIN 訊息

取得用來在按鈕控制項中繪製文字的邊界。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含用來繪製文字的邊界。

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



 

