---
title: 'XTYP_WILDCONNECT 交易 (Ddeml .h) '
description: 讓用戶端能夠在每個伺服器的服務名稱和主題名稱組上，建立符合指定服務名稱和主題名稱的交談。
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- XTYP_WILDCONNECT 交易資料 Exchange
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b2b170a8d2362dec6311f935a5bc0bb92fa16a9b04270afc59d8fe5ad5c19f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914728"
---
# <a name="xtyp_wildconnect-transaction"></a>XTYP \_ WILDCONNECT 交易

讓用戶端能夠在每個伺服器的服務名稱和主題名稱組上，建立符合指定服務名稱和主題名稱的交談。 當用戶端在 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)或 [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)函式的呼叫中指定 **null** 服務名稱、 **null** 主題名稱或兩者都指定時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
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

主題名稱的控制碼。 如果這個參數是 **Null**，用戶端會要求伺服器支援的所有主題名稱上進行交談。

</dd> <dt>

*hsz2* 
</dt> <dd>

服務名稱的控制碼。 如果這個參數是 **Null**，用戶端會要求伺服器支援的所有服務名稱上進行交談。

</dd> <dt>

*hdata* 
</dt> <dd>

未使用。

</dd> <dt>

*dwData1* 
</dt> <dd>

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)結構的指標，其中包含交談的內容資訊。 如果用戶端不是 DDEML 應用程式，此參數會設定為0。

</dd> <dt>

*dwData2* 
</dt> <dd>

指定用戶端是否與伺服器相同的應用程式實例。 如果參數是1，則用戶端會是相同的實例。 如果參數為0，則用戶端為不同的實例。

</dd> </dl>

## <a name="return-value"></a>傳回值

伺服器應傳回識別 [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) 結構陣列的資料控制碼。 陣列應針對符合用戶端所要求的服務名稱和主題名稱組的每個服務名稱和主題名稱組，各包含一個結構。 陣列必須以 **Null** 字串控制碼終止。 系統會將 [**XTYP \_ CONNECT \_ 確認**](xtyp-connect-confirm.md) 交易傳送到伺服器，以確認每個交談並將交談控制碼傳遞至伺服器。 如果伺服器在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ SKIP \_ CONNECT \_ 確認** 旗標，伺服器將不會收到這些確認。

伺服器應傳回 **Null** 以拒絕 **XTYP \_ WILDCONNECT** 交易。

## <a name="remarks"></a>備註

如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ FAIL \_ CONNECTIONS 連接** 旗標，則會篩選此交易。

伺服器無法封鎖此交易類型;\_會忽略 CBR 區塊傳回碼。

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

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

