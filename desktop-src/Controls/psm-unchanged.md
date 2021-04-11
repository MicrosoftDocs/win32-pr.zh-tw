---
title: 'PSM_UNCHANGED 訊息 (Prsht.idl .h) '
description: 通知屬性工作表，頁面中的資訊已還原為先前儲存的狀態。 您可以明確地傳送此訊息，或使用 PropSheet \_ 未變更宏。
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- PSM_UNCHANGED message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187309"
---
# <a name="psm_unchanged-message"></a>PSM \_ 未變更訊息

通知屬性工作表，頁面中的資訊已還原為先前儲存的狀態。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ 未**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) 變更宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

已還原為先前儲存狀態之頁面的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

如果沒有其他頁面已向屬性工作表註冊變更，屬性工作表會停用 [套用 **] 按鈕。**

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





