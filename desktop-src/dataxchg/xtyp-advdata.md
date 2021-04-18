---
title: 'XTYP_ADVDATA 交易 (Ddeml .h) '
description: 通知用戶端資料項目目的值已變更。 動態資料交換 (DDE) 用戶端回呼函式 DdeCallback，會在建立與伺服器的建議迴圈之後，接收此交易。
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965281"
---
# <a name="xtyp_advdata-transaction"></a>XTYP \_ ADVDATA 交易

通知用戶端資料項目目的值已變更。 動態資料交換 (DDE) 用戶端回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)，會在建立與伺服器的建議迴圈之後，接收此交易。


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>參數

<dl> <dt>

*uType* 
</dt> <dd>

交易類型。

</dd> <dt>

*uFmt* 
</dt> <dd>

從伺服器傳送之資料的格式 atom。

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

與主題名稱和專案名稱配對相關聯之資料的控制碼。 如果用戶端在要求「建議」迴圈時指定了 **XTYPF \_ NODATA** 旗標，則此參數為 **Null** 。

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

如果 DDE 回呼函數處理這項交易，則會傳回 **dde \_ FACK** ，如果它太忙碌而無法處理此交易，則會傳回 dde **\_ FBUSY** ; 如果拒絕此交易，則會傳回 dde **\_ FNOTPROCESSED** 。

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

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

