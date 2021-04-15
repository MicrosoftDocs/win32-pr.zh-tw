---
title: 'PSM_REBOOTSYSTEM 訊息 (Prsht.idl .h) '
description: 指出需要重新開機系統，變更才會生效。 您可以 \_ 明確地傳送 PSM REBOOTSYSTEM 訊息或使用 PropSheet \_ REBOOTSYSTEM 宏。
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464869"
---
# <a name="psm_rebootsystem-message"></a>PSM \_ REBOOTSYSTEM 訊息

指出需要重新開機系統，變更才會生效。 您可以明確地傳送 **PSM \_ REBOOTSYSTEM** 訊息或使用 [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) 宏。

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

應用程式應該只傳送此訊息以回應 [PSN \_ APPLY](psn-apply.md) 或 [PSN \_ KILLACTIVE](psn-killactive.md) 通知訊息。

此訊息會使 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式傳回 ID \_ PSREBOOTSYSTEM 值，但只有在使用者按一下 [ **確定]** 按鈕以關閉屬性工作表時才會傳回。 應用程式必須負責重新開機系統，這可以使用 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) 函數來完成。

這則訊息會取代之前或之後的所有 [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) 訊息。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

