---
title: 'PSM_CANCELTOCLOSE 訊息 (Prsht.idl .h) '
description: 當應用程式在最近的 PSN 套用無法取消的通知之後，由應用程式傳送 \_ 。 您可以使用 PropSheet CancelToClose 宏明確地傳送此訊息 \_ 。
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105276"
---
# <a name="psm_canceltoclose-message"></a>PSM \_ CANCELTOCLOSE 訊息

當應用程式在最近的 PSN 套用無法取消的通知之後 [， \_ ](psn-apply.md) 由應用程式傳送。 您可以使用 [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) 宏明確地傳送此訊息。

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

沒有傳回值。

## <a name="remarks"></a>備註

**PSM \_CANCELTOCLOSE** 會停用 [ **取消** ] 按鈕，並將 [ **確定]** 按鈕的文字變更為 [關閉]。

大部分的屬性工作表等候執行無法復原的變更，直到收到 PSN 套用 \_ 通知為止。 不過，在某些情況下，屬性工作表可能會在標準 PSN 套用 \_ /PSN 重設順序之外進行無法復原的變更 \_ 。 其中一個範例是包含 [ **編輯** ] 按鈕的屬性工作表，可用來顯示編輯屬性的 subdialog 方塊。 當使用者按一下 **[確定]** 提交變更時，[屬性工作表] 頁面會有數個選項。

-   它可以記錄變更，但要等到收到 PSN 套用 \_ 通知才能套用變更。 這是慣用的方法。
-   它可以在離開 subdialog box 之後立即套用變更，但請記住原始設定。 如果 \_ 收到 PSN 重設通知，這些設定可以用來還原原始狀態。
-   它可以立即套用變更，而不會在收到 [PSN \_ 重設](psn-reset.md) 通知時嘗試還原原始設定。 不建議使用此方法，但如果變更太遠而無法達成其他兩個選項，則可能是必要的。

針對第三個選項，應用程式應該將 **PSM \_ CANCELTOCLOSE** 訊息傳送至屬性工作表。 這會向使用者指出，藉由按一下 [ **取消** ] 按鈕，就無法反轉使用 [subdialog] 方塊進行的變更。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





