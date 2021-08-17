---
title: 'INapEnforcementClientBinding 解除初始化方法 (NapEnforcementClient .h) '
description: 結束 NapAgent 服務。
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- 解除初始化方法 NAP
- 解除初始化方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，解除初始化方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613646eb169ab12c788cc294ab012962606a77b5f9fe5dfc8c041e6a4ad6fa35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940142"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>INapEnforcementClientBinding：：解除初始化方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientBinding：：解除初始化** 方法會結束 NapAgent 服務。

## <a name="syntax"></a>語法


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

NapAgent 會封鎖進一步處理，直到 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 和 [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) 介面上的所有現有呼叫都完成為止。 在此通話結束時，NapAgent 會釋放其在強制用戶端 COM 指標上的所有參考。

在呼叫此函式之前，enforcer 必須在其所有使用中的連接上呼叫 [**INapEnforcementClientBinding：： NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) ，如此一來，如果任何 SoH-Requests 為孤立的，sha 就可以收到通知。

強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





