---
title: 'XTYP_REGISTER 交易 (Ddeml .h) '
description: '\_每當動態資料交換管理程式庫 (DDEML) 伺服器應用程式使用 DdeNameService 函式來註冊服務名稱，或每當支援系統主題的非 DDEML 應用程式啟動時，動態資料交換 (DDE) 回呼函式 DdeCallback 會收到 XTYP REGISTER 交易類型。'
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER 交易資料 Exchange
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c4ffdb48b7a69109659e65d816b4ab146a1f38bde976e7f8330746f564bc64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544747"
---
# <a name="xtyp_register-transaction"></a>XTYP \_ 註冊交易

每當動態資料交換管理程式庫 (DDEML) 伺服器應用程式使用 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)函式來註冊服務名稱，或每當支援系統主題的非 DDEML 應用程式啟動時，動態資料交換 (DDE) 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會收到 **XTYP \_ REGISTER** 交易類型。


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

要註冊之基底服務名稱的控制碼。

</dd> <dt>

*hsz2* 
</dt> <dd>

要註冊之實例特定服務名稱的控制碼。

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

應用程式無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。

應用程式應該使用 *hsz1* 參數，將服務名稱新增至使用者可用的伺服器清單。 應用程式應該使用 *hsz2* 參數來識別已啟動的應用程式實例。

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

