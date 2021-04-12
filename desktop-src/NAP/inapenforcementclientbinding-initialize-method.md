---
title: 'INapEnforcementClientBinding Initialize 方法 (NapEnforcementClient .h) '
description: 自動啟動 NapAgent 服務。
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464829"
---
# <a name="inapenforcementclientbindinginitialize-method"></a>INapEnforcementClientBinding：： Initialize 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientBinding：： Initialize** 方法會自動啟動 NapAgent 服務。

## <a name="syntax"></a>語法


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

識別強制用戶端及其版本的 [**EnforcementEntityId**](nap-datatypes.md) 。

</dd> <dt>

*回呼* \[在\]
</dt> <dd>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)介面的 COM 指標，由 NapAgent 用來以通知/進程回呼強制用戶端。 NapAgent 會保存與這個介面相關聯之物件的參考，直到呼叫 [**INapEnforcementClientBinding：：解除初始化**](inapenforcementclientbinding-uninitialize-method.md) 為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                                         | Description                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                               | 作業成功。<br/>                                                  |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>                     | 許可權錯誤，拒絕存取。<br/>                                             |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>                      | 系統資源限制，無法執行操作。<br/>                       |
| <dl> <dt>**HRESULT (\_ 已初始化的錯誤 \_)**</dt> </dl> | 如果 enforcer 先前已初始化，則會傳回此錯誤碼。<br/> |
| <dl> <dt>**NAP \_ E \_ 未 \_ 註冊**</dt> </dl>              | 如果 enforcer 之前未註冊，則會傳回此錯誤碼。<br/>      |



 

## <a name="remarks"></a>備註

強制用戶端必須先呼叫 **INapEnforcementClientBinding：： Initialize** 方法，才能呼叫 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。

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

[**INapEnforcementClientBinding：：解除初始化**](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





