---
title: 'PSM_ISDIALOGMESSAGE 訊息 (Prsht.idl .h) '
description: 將訊息傳遞至屬性工作表對話方塊，並指出對話方塊是否已處理訊息。 您可以使用 PropSheet IsDialogMessage 宏明確地傳送此訊息 \_ 。
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f28d63e5586d3b083282db4e029551ce4e61d0ef997e36e3e874e9f032095b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088678"
---
# <a name="psm_isdialogmessage-message"></a>PSM \_ ISDIALOGMESSAGE 訊息

將訊息傳遞至屬性工作表對話方塊，並指出對話方塊是否已處理訊息。 您可以使用 [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

訊息 [**結構的**](/windows/win32/api/winuser/ns-winuser-msg) 指標，其中包含要檢查的訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已處理訊息，則傳回 **TRUE** ; 如果尚未處理訊息，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

您的訊息迴圈應該使用具有無訊息屬性工作表的 **PSM \_ ISDIALOGMESSAGE** 訊息，將訊息傳遞至 [屬性工作表] 對話方塊。 在支援 Unicode 的系統上，請使用 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 和 [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) 函數的 Unicode 版本 (**GetMessageW** 和 **PeekMessageW**) 來取得訊息。

如果傳回值指出已處理訊息，則不能將它傳遞給 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 或 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) 函數。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

