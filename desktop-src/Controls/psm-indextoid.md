---
title: 'PSM_INDEXTOID 訊息 (Prsht.idl .h) '
description: 取得屬性工作表頁面的索引，並傳回其資源識別碼。 您可以明確地傳送此訊息，或使用 PropSheet \_ IndexToId 宏。
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- PSM_INDEXTOID message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025249"
---
# <a name="psm_indextoid-message"></a>PSM \_ INDEXTOID 訊息

取得屬性工作表頁面的索引，並傳回其資源識別碼。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的頁面索引。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 *wParam* 所指定之屬性工作表頁面的資源識別碼。 否則，它會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





