---
title: 'XTYP_EXECUTE 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ EXECUTE transaction 將命令字串傳送至伺服器。 當用戶端 \_ 在 DdeClientTransaction 函數中指定 XTYP EXECUTE 時，動態資料交換 (DDE) server 回呼函式 DdeCallback 會接收此交易。
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- XTYP_EXECUTE 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025351"
---
# <a name="xtyp_execute-transaction"></a>XTYP \_ 執行交易

用戶端會使用 **XTYP \_ EXECUTE** transaction 將命令字串傳送至伺服器。 當用戶端在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函數中指定 **XTYP \_ EXECUTE** 時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>參數

<dl> <dt>

*uType* 
</dt> <dd>

交易類型。

</dd> <dt>

*uFmt* 
</dt> <dd>

未使用。

</dd> <dt>

*hconv* 
</dt> <dd>

交談的控制碼。

</dd> <dt>

*hsz1* 
</dt> <dd>

主題名稱的控制碼。

</dd> <dt>

*hsz2* 
</dt> <dd>

未使用。

</dd> <dt>

*hdata* 
</dt> <dd>

命令字串的控制碼。

</dd> <dt>

*dwData1* 
</dt> <dd>

未使用。

</dd> <dt>

*dwData2* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果伺服器回呼函式處理此交易，則會傳回 **dde \_ FACK** ，如果它太忙碌而無法處理此交易，則會傳回 dde **\_ FBUSY** ，如果拒絕此交易，則會傳回 dde **\_ FNOTPROCESSED** 。

## <a name="remarks"></a>備註

如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ FAIL \_ 執行** 旗標，則會篩選此交易。

應用程式必須釋放在此交易期間取得的資料控制碼。 但是，如果應用程式必須在回呼函數傳回之後處理字串，則應用程式必須複製與資料控制碼相關聯的命令字串。 應用程式可以使用 [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) 函數來複製資料。

因為大部分的用戶端應用程式預期伺服器應用程式會以同步方式執行 **XTYP \_ 執行** 交易，所以伺服器應該嘗試從 DDE 回呼函式內或藉由傳回 **CBR \_ 區塊** 傳回碼，來執行 **XTYP \_ 執行** 交易的所有處理。 如果 *hdata* 參數是指示伺服器終止的命令，伺服器應該在處理 **XTYP \_ EXECUTE** transaction 之後執行此動作。

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

