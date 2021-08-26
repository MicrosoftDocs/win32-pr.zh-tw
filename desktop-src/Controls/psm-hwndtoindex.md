---
title: 'PSM_HWNDTOINDEX 訊息 (Prsht.idl .h) '
description: 採用屬性工作表頁面的視窗控制碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 PropSheet \_ HwndToIndex 宏。
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- PSM_HWNDTOINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed61c958fb3a0b30ba7cf55d1040cac51caa67f460d329312fb0e798b016aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985828"
---
# <a name="psm_hwndtoindex-message"></a>PSM \_ HWNDTOINDEX 訊息

採用屬性工作表頁面的視窗控制碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

頁面視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 *wParam* 所指定之屬性工作表頁面的以零為基底的索引。 否則，它會傳回 -1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 





