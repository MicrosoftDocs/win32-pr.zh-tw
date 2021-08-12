---
title: 'XTYP_ADVSTART 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ ADVSTART 交易來建立與伺服器之間的建議迴圈。
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART 交易資料 Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb18bda3dce4db465045991e26cdc2d97ddd87ddc69c494ffaf103c566955da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544757"
---
# <a name="xtyp_advstart-transaction"></a>XTYP \_ ADVSTART 交易

用戶端會使用 **XTYP \_ ADVSTART** 交易來建立與伺服器之間的建議迴圈。 當用戶端將 **XTYP \_ ADVSTART** 指定為 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函數的 *wType* 參數時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a>參數

<dl> <dt>

*uType* 
</dt> <dd>

交易類型。

</dd> <dt>

*uFmt* 
</dt> <dd>

用戶端要求的資料格式。

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

專案名稱的控制碼。

</dd> <dt>

*hdata* 
</dt> <dd>

未使用。

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

伺服器回呼函數應該傳回 **TRUE** ，以允許指定之主題名稱和專案名稱組的建議迴圈，或使用 **FALSE** 來拒絕建議迴圈。 如果回呼函式傳回 **TRUE**，則在相同主題名稱和專案名稱組上，伺服器對 [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) 函式的任何後續呼叫都會導致系統傳送 [**XTYP \_ ADVREQ**](xtyp-advreq.md) 交易至伺服器。

## <a name="remarks"></a>備註

如果用戶端針對已建立的「建議」迴圈，在主題名稱、專案名稱和資料格式上要求「建議」迴圈，則 (DDEML) 的動態資料交換管理程式庫不會建立重複的「建議」迴圈，但改為改變「建議迴圈」旗標 (**XTYPF \_ ACKREQ** 和 **XTYPF \_ NODATA**) 以符合最新的要求。

如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式中指定了 **CBF \_ FAIL 「 \_ 建議**」旗標，則會篩選此交易。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Ddeml (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

