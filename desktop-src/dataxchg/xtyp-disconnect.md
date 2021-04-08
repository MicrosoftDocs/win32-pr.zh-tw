---
title: 'XTYP_DISCONNECT 交易 (Ddeml .h) '
description: '\_當交談中的應用程式夥伴使用 DdeDisconnect 函式來終止交談時，應用程式的動態資料交換 (DDE) 回呼函式 DdeCallback 會接收 XTYP 中斷連接交易。'
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- XTYP_DISCONNECT 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685615"
---
# <a name="xtyp_disconnect-transaction"></a>XTYP \_ 中斷連接交易

當交談中的應用程式夥伴使用 [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)函式來終止交談時，應用程式的動態資料交換 (DDE) 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收 **XTYP \_ 中斷連接** 交易。


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

已終止交談的控制碼。

</dd> <dt>

*hsz1* 
</dt> <dd>

未使用。

</dd> <dt>

*hsz2* 
</dt> <dd>

未使用。

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

指定交談中的夥伴是否為相同的應用程式實例。 如果這個參數是1，則夥伴是相同的實例。 如果此參數為0，則夥伴為不同的實例。

</dd> </dl>

## <a name="remarks"></a>備註

如果應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式中指定了 **CBF \_ 略過 \_ 中斷連接** 旗標，則會篩選此交易。

應用程式可以在處理此交易時呼叫 [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) 函式，以取得已終止交談的狀態。 在回呼函數傳回之後，交談控制碼會變成無效。

應用程式無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。

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

[**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

