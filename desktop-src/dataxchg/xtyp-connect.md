---
title: 'XTYP_CONNECT 交易 (Ddeml .h) '
description: 用戶端會使用 XTYP \_ CONNECT 交易來建立交談。
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT 交易資料 Exchange
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1ff7a7a79d8b61deef6b5f19b829e5c8dd8f4603c5f60c3b47d0a84b0603736
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793418"
---
# <a name="xtyp_connect-transaction"></a>XTYP \_ CONNECT 交易

用戶端會使用 **XTYP \_ CONNECT** 交易來建立交談。 當用戶端指定伺服器支援 (的服務名稱，以及在 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)函式的呼叫中) 非 **Null** 的主題名稱時，動態資料交換 (DDE) server 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收此交易。


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
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

主題名稱的控制碼。

</dd> <dt>

*hsz2* 
</dt> <dd>

服務名稱的控制碼。

</dd> <dt>

*hdata* 
</dt> <dd>

未使用。

</dd> <dt>

*dwData1* 
</dt> <dd>

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)結構的指標，其中包含交談的內容資訊。 如果用戶端不是 DDEML 應用程式，此參數為0。

</dd> <dt>

*dwData2* 
</dt> <dd>

指定用戶端是否與伺服器相同的應用程式實例。 如果參數是1，則用戶端會是相同的實例。 如果參數為0，則用戶端為不同的實例。

</dd> </dl>

## <a name="return-value"></a>傳回值

伺服器回呼函數應該傳回 **TRUE** ，以允許用戶端在指定的服務名稱和主題名稱組上建立交談，否則函數應該會傳回 **FALSE** 以拒絕交談。 如果回呼函式傳回 **TRUE** 且已成功建立交談，則系統會將 [**XTYP \_ CONNECT \_ 確認**](xtyp-connect-confirm.md)交易發出至伺服器的回呼函式，藉此將交談控制碼傳遞給伺服器 (除非伺服器在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式) 中指定了 **CBF \_ SKIP \_ CONNECT \_ 確認** 旗標。

## <a name="remarks"></a>備註

如果伺服器應用程式在 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函數中指定了 **CBF \_ FAIL \_ CONNECTIONS 連接** 旗標，則會篩選此交易。

伺服器無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。

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

**概念**
</dt> <dt>

[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

