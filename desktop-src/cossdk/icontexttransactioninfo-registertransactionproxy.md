---
description: 將 ITransactionProxy 的執行與目前的內容產生關聯。
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: ICoNtextTransactionInfo：： RegisterTransactionProxy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317932"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a>ICoNtextTransactionInfo：： RegisterTransactionProxy 方法

將 [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) 的執行與目前的內容產生關聯。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProxy* \[在\]
</dt> <dd>

要與目前內容建立關聯的 [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) 執行。

</dd> <dt>

*pGuid* \[擴展\]
</dt> <dd>

識別交易 proxy 的 GUID。 在交易 proxy 上呼叫 [**ITransactionProxy：： Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) 時，com + 會使用此 GUID。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY 和 e 非 \_ 預期的，以及下列值。



| 傳回碼                                                                                                     | Description                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                            | 已成功完成命令。<br/>                                                                           |
| <dl> <dt>**內容 \_ E \_ ALREADYINTRANSACTION**</dt> </dl> | 目前的內容已有相關聯的 [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) 執行。<br/> |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>                       | 目前的內容是裝載「攜帶您自己的交易」 (BYOT) 交易或非根交易。<br/>    |



 

## <a name="remarks"></a>備註

只有在目前的內容是根交易內容時，才能呼叫 **RegisterTransactionProxy** 方法。 如果內容裝載 BYOT 交易或非根交易，則無法呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




