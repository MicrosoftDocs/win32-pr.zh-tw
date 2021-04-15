---
title: 'CQPM_SETDEFAULTPARAMETERS 訊息 (Cmnquery .h) '
description: 傳送至查詢表單延伸頁面的 CQPageProc 回呼函數，以設定頁面的替代預設參數。
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- CQPM_SETDEFAULTPARAMETERS 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465157"
---
# <a name="cqpm_setdefaultparameters-message"></a>CQPM \_ SETDEFAULTPARAMETERS 訊息

**CQPM \_ SETDEFAULTPARAMETERS** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)回呼函數，以設定頁面的替代預設參數。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

如果頁面為預設頁面，則包含非零，否則為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)結構的指標，其中包含 [目錄服務查詢] 對話方塊的相關資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息的傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Cmnquery。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





