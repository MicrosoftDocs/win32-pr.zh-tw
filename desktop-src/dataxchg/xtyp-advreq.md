---
title: 'XTYP_ADVREQ 交易 (Ddeml .h) '
description: XTYP \_ ADVREQ transaction 會通知伺服器，指定的主題名稱和專案名稱組上的建議交易未完成，而且對應至主題名稱和專案名稱組的資料已經變更。
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384782"
---
# <a name="xtyp_advreq-transaction"></a>XTYP \_ ADVREQ 交易

**XTYP \_ ADVREQ** transaction 會通知伺服器，指定的主題名稱和專案名稱組上的建議交易未完成，而且對應至主題名稱和專案名稱組的資料已經變更。 當伺服器呼叫 [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)函式之後，系統會將此交易傳送給動態資料交換 (DDE) 回呼函數 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)。


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>參數

<dl> <dt>

*uType* 
</dt> <dd>

交易類型。

</dd> <dt>

*uFmt* 
</dt> <dd>

應將資料提交至用戶端的格式。

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

已變更之專案名稱的控制碼。

</dd> <dt>

*hdata* 
</dt> <dd>

未使用。

</dd> <dt>

*dwData1* 
</dt> <dd>

在低序位單字中， **XTYP \_ ADVREQ** 交易的計數，這些交易仍會在目前呼叫 [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) 函式的內容中設定的相同主題、專案和格式名稱上進行處理。 如果目前的 **XTYP \_ ADVREQ** 交易是最後一個交易，則此計數為零。 伺服器可以使用此計數來判斷是否要建立建議資料的 **HDATA \_ APPOWNED** 資料控制碼。

如果 DDEML 發出 **XTYP \_ ADVREQ** 交易，則低序位單字會設定為 **CADV \_ LATEACK** ，因為 \_ 來自伺服器所 outrun 的用戶端會收到延遲抵達的 DDE ACK 訊息。

未使用高序位字組。

</dd> <dt>

*dwData2* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

伺服器應該先呼叫 [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) 函數來建立資料控制碼，以識別已變更的資料，然後傳回控制碼。 如果伺服器無法完成交易，則應該傳回 **Null** 。

## <a name="remarks"></a>備註

伺服器無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。

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

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

