---
title: 'INapSystemHealthValidationRequest GetMachineName 方法 (NapSystemHealthValidator .h) '
description: 系統健康狀態驗證 (Shv) 用來取出 NAP 用戶端的電腦名稱稱。 然後，SHV 會記錄這些資訊。
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- GetMachineName 方法 NAP
- GetMachineName 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetMachineName 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106506"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a>INapSystemHealthValidationRequest：： GetMachineName 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidationRequest：： GetMachineName** 方法是由系統健康狀態驗證 (shv) 用來取出 NAP 用戶端的電腦名稱稱。 然後，SHV 會記錄這些資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*machineName* \[擴展\]
</dt> <dd>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含 NAP 用戶端的電腦名稱稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





