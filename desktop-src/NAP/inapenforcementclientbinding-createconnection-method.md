---
title: 'INapEnforcementClientBinding CreateConnection 方法 (NapEnforcementClient .h) '
description: Enforcers 用來建立連線物件。
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- CreateConnection 方法 NAP
- CreateConnection 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，CreateConnection 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72c8ef4760d611c45291f0de1039b915e9bc8fedde94c314bb1272e4b99b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891278"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a>INapEnforcementClientBinding：： CreateConnection 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

Enforcers 會使用 **INapEnforcementClientBinding：： CreateConnection** factory 方法來建立連線物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*連接* \[擴展\]
</dt> <dd>

NAP 系統傳回的新 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 介面的 COM 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





