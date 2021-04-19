---
title: 'XTYP_ADVSTOP 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ ADVSTOP 交易，以伺服器結束「建議」迴圈。 當用戶端 \_ 在 DdeClientTransaction 函數中指定 XTYP ADVSTOP 時，動態資料交換 (DDE) server 回呼函式 DdeCallback 會接收此交易。
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979681"
---
# <a name="xtyp_advstop-transaction"></a>XTYP \_ ADVSTOP 交易

用戶端會使用 **XTYP \_ ADVSTOP** 交易，以伺服器結束「建議」迴圈。 當用戶端在 [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)函數中指定 **XTYP \_ ADVSTOP** 時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a>參數

<dl> <dt>

*uType* 
</dt> <dd>

交易類型。

</dd> <dt>

*uFmt* 
</dt> <dd>

與要結束的建議迴圈相關聯的資料格式。

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

## <a name="remarks"></a>備註

如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式中指定了 **CBF \_ FAIL 「 \_ 建議**」旗標，則會篩選此交易。

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

