---
title: 'LB_SETHORIZONTALEXTENT 訊息 (Winuser .h) '
description: 設定以圖元為單位的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844111"
---
# <a name="lb_sethorizontalextent-message"></a>LB \_ SETHORIZONTALEXTENT 訊息

設定以圖元為單位的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。 如果清單方塊的寬度小於此值，水準捲軸會水準滾動清單方塊中的專案。 如果清單方塊的寬度等於或大於此值，則會隱藏水準捲軸。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定清單方塊可滾動的圖元數。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

若要回應 **LB \_ SETHORIZONTALEXTENT** 訊息，必須使用 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式來定義清單方塊。

請注意，清單方塊不會動態更新其水準範圍。

此訊息對多欄清單方塊沒有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md)
</dt> </dl>

 

