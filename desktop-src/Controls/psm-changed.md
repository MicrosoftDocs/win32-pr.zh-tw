---
title: 'PSM_CHANGED 訊息 (Prsht.idl .h) '
description: 通知屬性工作表，頁面中的資訊已變更。 您可以使用 PropSheet Changed 宏明確地傳送此訊息 \_ 。
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- PSM_CHANGED 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2002801d21e4e89a6ccf762b9c9932671b210217a950f5494fb736feda35d32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826018"
---
# <a name="psm_changed-message"></a>PSM \_ 變更訊息

通知屬性工作表，頁面中的資訊已變更。 您可以使用 [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

已變更頁面的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

屬性工作表會啟用 [套用 **] 按鈕。**

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





