---
title: 'CQPM_INITIALIZE 訊息 (Cmnquery .h) '
description: 當頁面新增至表單時，傳送至查詢表單延伸頁面的 CQPageProc 回呼函式。
ms.assetid: 29cb39d5-9bc4-472e-8a2f-dc6cd505144a
ms.tgt_platform: multiple
keywords:
- CQPM_INITIALIZE 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_INITIALIZE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e95c7087a9cd2d40387c8d7dd07aa93c8f697fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025040"
---
# <a name="cqpm_initialize-message"></a>CQPM \_ INITIALIZE 訊息

當頁面新增至表單時， **CQPM \_ INITIALIZE** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) 回呼函式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。

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
</dt> </dl>

 

 





