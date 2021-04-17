---
title: 'INapEnforcementClientBinding NotifySoHChangeFailure 方法 (NapEnforcementClient .h) '
description: 由強制用戶端用來通知 NapAgent，它無法處理先前的 INapEnforcementClientCallback NotifySoHChange。
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- NotifySoHChangeFailure 方法 NAP
- NotifySoHChangeFailure 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，NotifySoHChangeFailure 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467005"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a>INapEnforcementClientBinding：： NotifySoHChangeFailure 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientBinding：： NotifySoHChangeFailure** 方法是由強制用戶端用來通知 NapAgent 它無法處理先前的 [**INapEnforcementClientCallback：： NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)。

## <a name="syntax"></a>語法


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                             | Description                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                   | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>         | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>          | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**NAP \_ E \_ 未 \_ 初始化**</dt> </dl> | Enforcer 先前尚未初始化。<br/>       |



 

## <a name="remarks"></a>備註

由於這個方法會呼叫 [**INapEnforcementClientCallback：： NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) ，因此在稍後呼叫 NapAgent 時，會重新嘗試套用 SoH 變更。 一旦強制用戶端呼叫 [**INapEnforcementClientBinding：： GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)之後，就必須套用變更，也就是在這個時間點之後，NapAgent 不會處理任何失敗。

強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





