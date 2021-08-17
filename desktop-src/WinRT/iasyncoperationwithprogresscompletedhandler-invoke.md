---
description: 叫用指定的非同步作業報告進度時，所呼叫的方法。
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: IAsyncOperationWithProgressCompletedHandler<TResult，TProgress>：： Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 141f79398e1f9f250b402df130daa728c8e2f0e5f78702d7866dbe9a202b5978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323117"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>IAsyncOperationWithProgressCompletedHandler<TResult，TProgress>：： Invoke 方法

叫用指定的非同步作業報告進度時，所呼叫的方法。

## <a name="syntax"></a>語法


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*system.runtime.interopservices.windowsruntime.asyncinfo* \[在\]
</dt> <dd>

類型： **[ **IAsyncOperationWithProgress<TResult，TProgress>**](/previous-versions//br205807(v=vs.85))\***

報告完成的非同步動作。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>           |
| 最低支援的伺服器<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAsyncOperationWithProgressCompletedHandler<TResult，TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 
