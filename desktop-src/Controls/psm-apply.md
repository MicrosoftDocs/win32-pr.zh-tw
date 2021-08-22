---
title: 'PSM_APPLY 訊息 (Prsht.idl .h) '
description: 模擬 [套用] 按鈕的選取專案，表示一或多個頁面已變更，而且需要驗證和記錄變更。
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f753eb2465ec835f467493bdbd83d10b8ba174b11c83abffcb91d20f8beba002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544158"
---
# <a name="psm_apply-message"></a>PSM 套用 \_ 訊息

模擬 **[套用] 按鈕的** 選取專案，表示一或多個頁面已變更，而且需要驗證和記錄變更。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果所有頁面都成功套用變更，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

屬性工作表會將 [PSN \_ KILLACTIVE](psn-killactive.md) 通知程式碼傳送至目前的頁面。 如果目前的頁面傳回 **FALSE**，則屬性工作表會將 [PSN \_](psn-apply.md) 套用通知程式碼至所有使用中頁面。 您可以 \_ 使用 [**PropSheet \_ apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) 宏明確地傳送 PSM 套用訊息。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





