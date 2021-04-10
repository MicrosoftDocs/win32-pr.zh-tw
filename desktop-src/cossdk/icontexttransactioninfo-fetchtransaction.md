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
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110916"
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
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




