---
title: 'BCM_SETTEXTMARGIN 訊息 (Commctrl .h) '
description: BCM \_ SETTEXTMARGIN 訊息會設定在按鈕控制項中繪製文字的邊界。
ms.assetid: 0798b1c5-7db4-46c6-8881-4c847abc7460
keywords:
- BCM_SETTEXTMARGIN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724c3e16c19aa2fb146bc0b47dec563db8b871536cb8f7e58fc86cbb739c225c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921358"
---
# <a name="bcm_settextmargin-message"></a>BCM \_ SETTEXTMARGIN 訊息

**BCM \_ SETTEXTMARGIN** 訊息會設定在按鈕控制項中繪製文字的邊界。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，指定用來繪製文字的邊界。

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**按鈕 \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)
</dt> <dt>

**概念**
</dt> <dt>

[按鈕](buttons.md)
</dt> </dl>

 

