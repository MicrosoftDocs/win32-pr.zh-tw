---
title: 'PSM_PRESSBUTTON 訊息 (Prsht.idl .h) '
description: 模擬屬性工作表按鈕的選取專案。 您可以使用 PropSheet PressButton 宏明確地傳送此訊息 \_ 。
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- PSM_PRESSBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467104"
---
# <a name="psm_pressbutton-message"></a>PSM \_ PRESSBUTTON 訊息

模擬屬性工作表按鈕的選取專案。 您可以使用 [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要選取之按鈕的索引。 此參數可以是下列其中一個值。



| 值                                                                                                                                                            | 意義                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <dt>**PSBTN \_ APPLYNOW**</dt> </dl> | 選取 [ **套用** ] 按鈕。 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，此值無效。<br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <dt>**PSBTN \_ 回來**</dt> </dl>             | 選取 [ **上一步** ] 按鈕。<br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <dt>**PSBTN \_ 取消**</dt> </dl>       | 選取 [ **取消** ] 按鈕。<br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <dt>**PSBTN \_ 完成**</dt> </dl>       | 選取 [ **完成]** 按鈕。<br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <dt>**PSBTN \_ 說明**</dt> </dl>             | 選取 [ **說明** ] 按鈕。 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，此值無效。<br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <dt>**PSBTN \_ 下一步**</dt> </dl>             | 選取 [ **下一步]** 按鈕。<br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <dt>**PSBTN \_ 確定**</dt> </dl>                   | 選取 [ **確定]** 按鈕。 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，此值無效。<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





