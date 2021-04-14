---
title: 'CQPM_HANDLERSPECIFIC 訊息 (Cmnquery .h) '
description: 用於查詢處理常式私用之訊息的基底值。
ms.assetid: c3badb89-ee4e-4317-97aa-15187b9bb3e8
ms.tgt_platform: multiple
keywords:
- CQPM_HANDLERSPECIFIC 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_HANDLERSPECIFIC
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed06d4bd2b33eaf6224bb72f4814dfdced5cce2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464553"
---
# <a name="cqpm_handlerspecific-message"></a>CQPM \_ HANDLERSPECIFIC 訊息

**CQPM \_ HANDLERSPECIFIC** 訊息是用於查詢處理常式私用之訊息的基底值。 查詢處理常式應該將此值新增至私用訊息，以確保不會發生訊息衝突。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含其他訊息資料。 此參數的內容是由查詢處理常式所定義。

</dd> <dt>

*lParam* 
</dt> <dd>

包含其他訊息資料。 此參數的內容是由查詢處理常式所定義。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值的意義是由查詢處理常式所定義。

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

 

 





