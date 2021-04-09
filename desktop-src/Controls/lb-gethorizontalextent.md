---
title: 'LB_GETHORIZONTALEXTENT 訊息 (Winuser .h) '
description: 取得清單方塊可水準滾動 (可滾動寬度的寬度（以圖元為單位）) 如果清單方塊具有水準捲軸。
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935014"
---
# <a name="lb_gethorizontalextent-message"></a>LB \_ GETHORIZONTALEXTENT 訊息

取得清單方塊可水準滾動 (可滾動寬度的寬度（以圖元為單位）) 如果清單方塊具有水準捲軸。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是清單方塊的可滾動寬度（以圖元為單位）。

## <a name="remarks"></a>備註

若要回應 **LB \_ GETHORIZONTALEXTENT** 訊息，必須使用 [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) 樣式來定義清單方塊。

如果應用程式未設定清單方塊的水準範圍 (使用 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)) ，則預設的水準範圍為零。 請注意，清單方塊不會動態更新其水準範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

