---
title: 'CBCreateClientInstance 函式 (Cbclient) '
description: 建立遠端桌面連線代理人 RPC 用戶端的實例。
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- CBCreateClientInstance 函式遠端桌面服務
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001016"
---
# <a name="cbcreateclientinstance-function"></a>CBCreateClientInstance 函式

建立遠端桌面連線代理人 RPC 用戶端的實例。

## <a name="syntax"></a>語法


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*版本* \[在\]
</dt> <dd>

指定所要求遠端桌面連線代理人用戶端介面的版本。 這必須是下列值。

<dt>

1
</dt> <dd>

遠端桌面連線代理人用戶端的第1版。

</dd> </dl> </dd> <dt>

*ppCbClient* \[擴展\]
</dt> <dd>

接收遠端桌面連線代理人用戶端物件之 [**IConnectionBrokerClient**](iconnectionbrokerclient.md) 介面指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cbclient。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Cbclient .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





