---
title: 'HDM_GETITEMDROPDOWNRECT 訊息 (Commctrl .h) '
description: 取得具有樣式 HDF SPLITBUTTON 的標頭專案之分割按鈕的周框 \_ 。 明確地傳送此訊息，或使用標頭 \_ GetItemDropDownRect 宏。
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- HDM_GETITEMDROPDOWNRECT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025128"
---
# <a name="hdm_getitemdropdownrect-message"></a>HDM \_ GETITEMDROPDOWNRECT 訊息

取得具有樣式 **HDF \_ SPLITBUTTON** 的標頭專案之分割按鈕的周框。 明確地傳送此訊息，或使用 [**標頭 \_ GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

以零為基底的標頭控制項專案索引，為其取得周框矩形。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

[**矩形**](/windows/win32/api/windef/ns-windef-rect)的指標，此結構會接收周框的資訊。 訊息寄件者負責配置此結構。 在矩形結構中傳回的座標會以相對於標題控制項父系的方式表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

標頭專案必須具有 style **HDF \_ SPLITBUTTON**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於標題控制項](header-controls.md)
</dt> </dl>

 

 





