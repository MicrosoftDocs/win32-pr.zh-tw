---
title: 'INapEnforcementClientBinding GetSoHRequest 方法 (NapEnforcementClient .h) '
description: 由強制用戶端用來取得特定連接的 SoH 要求。
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 780f144c6f4613006940069896aa8382006b179631acd83283121ee3c64ec0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134334"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>INapEnforcementClientBinding：： GetSoHRequest 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientBinding：： GetSoHRequest** 方法是由強制用戶端用來取得特定連接的 SoH 要求。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*連接* \[在\]
</dt> <dd>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)介面的 COM 指標。 在方法完成之後，NapAgent 不會保留與這個介面相關聯之物件的參考。

</dd> <dt>

*retriggerHint* \[擴展\]
</dt> <dd>

**布林** 值的指標，指出是否應該重新觸發連接。 如果自上次呼叫此函式之後，或 [**ProbationTime**](nap-datatypes.md)已過期， [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)已變更，則為 **TRUE** 。 否則會傳回 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                             | 描述                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                   | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>         | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>          | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**NAP \_ E \_ 未 \_ 初始化**</dt> </dl> | Enforcer 先前尚未初始化。<br/>       |



 

## <a name="remarks"></a>備註

NapAgent 會在連線物件上設定 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。

如果這個連線上的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 未完成，則會捨棄它，而 sha 會收到孤立 **SoHRequests** 的通知。

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
</dt> </dl>

 

 





