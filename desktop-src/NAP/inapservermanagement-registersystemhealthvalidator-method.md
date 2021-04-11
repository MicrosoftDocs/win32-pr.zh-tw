---
title: 'INapServerManagement RegisterSystemHealthValidator 方法 (NapServerManagement .h) '
description: 註冊 SHV。
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- RegisterSystemHealthValidator 方法 NAP
- RegisterSystemHealthValidator 方法 NAP，INapServerManagement 介面
- INapServerManagement 介面 NAP，RegisterSystemHealthValidator 方法
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187322"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>INapServerManagement：： RegisterSystemHealthValidator 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapServerManagement：： RegisterSystemHealthValidator** 方法會註冊 SHV。

## <a name="syntax"></a>語法


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*驗證* \[ 程式在\]
</dt> <dd>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)結構的指標，其中包含 SHV 註冊資訊。

</dd> <dt>

*validatorClsid* \[在\]
</dt> <dd>

COM 類別 CLSID 的指標，該類別會實 [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                  | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>        | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>         | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**NAP \_ E \_ 衝突 \_ 識別碼**</dt> </dl> | SHV 識別碼已註冊。<br/>                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                               |
| 標頭<br/>                   | <dl> <dt>NapServerManagement。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





