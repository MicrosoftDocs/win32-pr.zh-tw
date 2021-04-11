---
title: 'PSM_IDTOINDEX 訊息 (Prsht.idl .h) '
description: 取得屬性工作表頁面的資源識別碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 PropSheet \_ IdToIndex 宏。
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- PSM_IDTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105275"
---
# <a name="psm_idtoindex-message"></a>PSM \_ IDTOINDEX 訊息

取得屬性工作表頁面的資源識別碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

頁面的資源識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 *lParam* 所指定之屬性工作表頁面的以零為基底的索引。 否則，它會傳回 -1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





