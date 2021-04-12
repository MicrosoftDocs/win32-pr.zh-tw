---
title: 'CB_SETHORIZONTALEXTENT 訊息 (Winuser .h) '
description: 應用程式會傳送 CB \_ SETHORIZONTALEXTENT 訊息，以圖元為單位來設定捲軸的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- CB_SETHORIZONTALEXTENT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465249"
---
# <a name="cb_sethorizontalextent-message"></a>CB \_ SETHORIZONTALEXTENT 訊息

應用程式會傳送 **CB \_ SETHORIZONTALEXTENT** 訊息，以圖元為單位來設定捲軸的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。 如果清單方塊的寬度小於此值，水準捲軸會水準滾動清單方塊中的專案。 如果清單方塊的寬度等於或大於此值，則會隱藏水準捲軸，或者，如果下拉式方塊的 [**CBS \_ DISABLENOSCROLL**](combo-box-styles.md) 樣式為停用。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定清單方塊的可滾動寬度（以圖元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ GETHORIZONTALEXTENT**](cb-gethorizontalextent.md)
</dt> </dl>

 

 





