---
title: 'XTYP_CONNECT_CONFIRM 交易 (Ddeml .h) '
description: 動態資料交換 (的 DDE) server 回呼函式 DdeCallback，會收到 XTYP \_ CONNECT \_ confirm 交易，以確認已與用戶端建立交談，以及為伺服器提供交談控制碼。
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384778"
---
# <a name="xtyp_connect_confirm-transaction"></a>XTYP \_ CONNECT \_ 確認交易

動態資料交換 (的 DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)，會收到 **XTYP \_ CONNECT \_ confirm** 交易，以確認已與用戶端建立交談，以及為伺服器提供交談控制碼。 由於先前的 [**XTYP \_ CONNECT**](xtyp-connect.md) 或 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易的結果，系統會傳送此交易。


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

新對話的控制碼。

</dd> <dt>

*hsz1* 
</dt> <dd>

已建立交談之主題名稱的控制碼。

</dd> <dt>

*hsz2* 
</dt> <dd>

已建立交談之服務名稱的控制碼。

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

指定用戶端是否與伺服器相同的應用程式實例。 如果參數是1，則用戶端會是相同的實例。 如果參數為0，則用戶端為不同的實例。

</dd> </dl>

## <a name="remarks"></a>備註

如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ SKIP \_ CONNECT \_ 確認** 旗標，則會篩選此交易。

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

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

