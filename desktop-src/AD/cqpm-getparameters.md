---
title: 'CQPM_GETPARAMETERS 訊息 (Cmnquery .h) '
description: 傳送至查詢表單延伸頁面的 CQPageProc 回呼函數，以抓取頁面所執行之查詢的相關資料。
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- CQPM_GETPARAMETERS 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64713c79fc2c1b72f1962363f1330ecd794ad804f0ab084b66c134c66133cd82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021229"
---
# <a name="cqpm_getparameters-message"></a>CQPM \_ GETPARAMETERS 訊息

**CQPM \_ GETPARAMETERS** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)回呼函數，以抓取頁面所執行之查詢的相關資料。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)值的指標，此值會接收頁面所執行之查詢的相關資料。 如果這個參數是 **Null**，則 **DSQUERYPARAMS** 結構必須由擴充功能使用 [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) 函式來配置。

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

[**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

