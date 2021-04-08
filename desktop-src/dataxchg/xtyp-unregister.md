---
title: 'XTYP_UNREGISTER 交易 (Ddeml .h) '
description: '\_當動態資料交換管理程式庫 (DDEML) 伺服器應用程式使用 DdeNameService 函式取消註冊服務名稱，或每次支援系統主題的非 DDEML 應用程式終止時，動態資料交換 (DDE) 回呼函式 DdeCallback 會接收 XTYP 取消註冊交易。'
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- XTYP_UNREGISTER 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686250"
---
# <a name="xtyp_unregister-transaction"></a>XTYP \_ 取消註冊交易

當動態資料交換管理程式庫 (DDEML) 伺服器應用程式使用 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)函式取消註冊服務名稱，或每次支援系統主題的非 DDEML 應用程式終止時，動態資料交換 (DDE) 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收 **XTYP \_ 取消註冊** 交易。


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

未使用。

</dd> <dt>

*hsz1* 
</dt> <dd>

要取消註冊之基底服務名稱的控制碼。

</dd> <dt>

*hsz2* 
</dt> <dd>

要取消註冊之實例特定服務名稱的控制碼。

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

## <a name="remarks"></a>備註

如果應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ SKIP \_ 註冊** 旗標，則會篩選此交易。

應用程式無法封鎖此交易類型;\_會忽略 CBR 區塊傳回碼。

應用程式應該使用 *hsz1* 參數，將服務名稱從使用者可用的伺服器清單中移除。 應用程式應該使用 *hsz2* 參數來識別已終止的應用程式實例。

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

