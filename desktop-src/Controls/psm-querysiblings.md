---
title: 'PSM_QUERYSIBLINGS 訊息 (Prsht.idl .h) '
description: 傳送至屬性工作表，然後將訊息轉送到其每個頁面。 您可以使用 PropSheet QuerySiblings 宏明確地傳送此訊息 \_ 。
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c270a3c7a667894f7821f6c0c169115846b6ddc2492648f5f9d75a0c85d21d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088648"
---
# <a name="psm_querysiblings-message"></a>PSM \_ QUERYSIBLINGS 訊息

傳送至屬性工作表，然後將訊息轉送到其每個頁面。 您可以使用 [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

第一個應用程式定義的參數。

</dd> <dt>

*lParam* 
</dt> <dd>

第二個應用程式定義的參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

從屬性工作表中的頁面傳回非零值; 如果沒有頁面傳回非零值，則為零。

## <a name="remarks"></a>備註

如果頁面傳回非零值，則屬性工作表不會將訊息傳送至後續頁面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





