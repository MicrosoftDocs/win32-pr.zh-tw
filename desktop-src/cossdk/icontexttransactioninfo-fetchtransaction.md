---
description: 抓取與目前內容相關聯的交易或交易 proxy （如果有的話）。
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: ICoNtextTransactionInfo：： FetchTransaction 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d673483118feb02ec2f1172640b9972d883505f48bc1fd8d8803844b963b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991058"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>ICoNtextTransactionInfo：： FetchTransaction 方法

抓取與目前內容相關聯的交易或交易 proxy （如果有的話）。

## <a name="syntax"></a>語法


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pUnk* \[退出，retval\]
</dt> <dd>

與目前內容相關聯的交易或交易 proxy;否則 **為 Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期和 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




