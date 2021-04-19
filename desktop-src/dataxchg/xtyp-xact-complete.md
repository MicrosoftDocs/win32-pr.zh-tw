---
title: 'XTYP_XACT_COMPLETE 交易 (Ddeml .h) '
description: '\_ \_ 當非同步交易（由 DdeClientTransaction 函式的呼叫所起始）完成時，動態資料交換 (DDE) 用戶端回呼函式 DdeCallback 會接收 XTYP 的交易完成交易。'
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969762"
---
# <a name="xtyp_xact_complete-transaction"></a>XTYP \_ \_ 交易完成交易

當非同步交易（由 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函式的呼叫所起始）完成時，動態資料交換 (DDE) 用戶端回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收 XTYP 的交易 **\_ \_ 完成** 交易。


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a>參數

<dl> <dt>

*uType* 
</dt> <dd>

交易類型。

</dd> <dt>

*uFmt* 
</dt> <dd>

與已完成之交易相關聯的資料格式 (（如果適用) ），如果在交易期間未交換任何資料，則 **為 Null** 。

</dd> <dt>

*hconv* 
</dt> <dd>

交談的控制碼。

</dd> <dt>

*hsz1* 
</dt> <dd>

與已完成之交易相關之主題名稱的控制碼。

</dd> <dt>

*hsz2* 
</dt> <dd>

與已完成之交易相關之專案名稱的控制碼。

</dd> <dt>

*hdata* 
</dt> <dd>

已完成之交易中相關資料的控制碼（如果適用）。 如果交易成功但未包含任何資料，則此參數為 **TRUE**。 如果交易失敗，此參數為 **Null** 。

</dd> <dt>

*dwData1* 
</dt> <dd>

已完成之交易的交易識別碼。

</dd> <dt>

*dwData2* 
</dt> <dd>

低字組中任何適用的 **DDE \_** 狀態旗標。 此參數可支援相依于 **DDE \_ APPSTATUS** 位的應用程式。 建議應用程式不再使用這些位，在未來的 DDEML 版本中可能不受支援。

</dd> </dl>

## <a name="remarks"></a>備註

應用程式不能釋放在此交易期間取得的資料控制碼。 但是，如果應用程式必須在回呼函數傳回之後處理資料，則應用程式必須複製與資料控制碼相關聯的資料。 應用程式可以使用 [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) 函數來複製資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Ddeml (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

