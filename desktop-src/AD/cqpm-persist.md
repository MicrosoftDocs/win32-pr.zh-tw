---
title: 'CQPM_PERSIST 訊息 (Cmnquery .h) '
description: 傳送至查詢表單延伸頁面的 CQPageProc 回呼函式，以允許頁面讀取或寫入持續性記憶體中的查詢資料。
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- CQPM_PERSIST 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66eeeba5f80397aa422c465cb224064c58a4544f4d64ae2fba3bed5030b1c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020968"
---
# <a name="cqpm_persist-message"></a>CQPM \_ 保存訊息

**CQPM \_ 保存** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)回呼函式，以允許頁面讀取或寫入持續性記憶體中的查詢資料。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

包含非零值，可讀取查詢資料或零來寫入查詢資料。

</dd> <dt>

*lParam* 
</dt> <dd>

應從中讀取或寫入查詢資料之 [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) 介面的指標。

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
</dt> <dt>

[**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

