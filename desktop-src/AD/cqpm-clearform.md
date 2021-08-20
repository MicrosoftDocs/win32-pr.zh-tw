---
title: 'CQPM_CLEARFORM 訊息 (Cmnquery .h) '
description: 當頁面內容應該重設為預設值時，傳送至擴充功能頁面查詢的 CQPageProc 回呼函式。
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- CQPM_CLEARFORM 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f900542c631193057985ca70d81dbfa7d3e53c6602f81a69b4e61a7cd107641a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021364"
---
# <a name="cqpm_clearform-message"></a>CQPM \_ CLEARFORM 訊息

當頁面內容應該重設為預設值時，會將 **CQPM \_ CLEARFORM** 訊息傳送至擴充功能頁面的查詢 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) 回呼函數。

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

如果 **成功 \_ ，則傳回** ，否則會傳回標準的 **HRESULT** 錯誤碼。

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

 

 





