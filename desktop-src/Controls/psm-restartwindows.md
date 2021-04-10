---
title: 'PSM_RESTARTWINDOWS 訊息 (Prsht.idl .h) '
description: 指出必須重新開機 Windows，變更才會生效。
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- PSM_RESTARTWINDOWS message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843424"
---
# <a name="psm_restartwindows-message"></a>PSM \_ RESTARTWINDOWS 訊息

指出必須重新開機 Windows，變更才會生效。

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

應用程式應該只傳送此訊息以回應 [PSN \_ APPLY](psn-apply.md) 或 [PSN \_ KILLACTIVE](psn-killactive.md) 通知碼。 您可以明確地傳送 **PSM \_ RESTARTWINDOWS** 訊息或使用 [**PropSheet \_ RESTARTWINDOWS**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) 宏。

此訊息會使 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式傳回 ID \_ PSRESTARTWINDOWS 值，但只有在使用者按一下 [ **確定]** 按鈕以關閉屬性工作表時才會傳回。 應用程式需要重新開機 Windows 的責任，您可以使用 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) 函式來完成這項工作。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

