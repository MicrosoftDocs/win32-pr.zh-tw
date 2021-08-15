---
title: 'INapSystemHealthValidationRequest GetStringCorrelationId 方法 (NapSystemHealthValidator .h) '
description: 系統健康狀態驗證會使用 (Shv) 必須記錄這項資訊。
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- GetStringCorrelationId 方法 NAP
- GetStringCorrelationId 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetStringCorrelationId 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5818ebd219dd38633da92a269e63d5641f393371cfa67b6910844523c37929ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939359"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a>INapSystemHealthValidationRequest：： GetStringCorrelationId 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidationRequest：： GetStringCorrelationId** 方法是由系統健康狀態驗證 (shv 所使用) 必須記錄這項資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*correlationId* \[擴展\]
</dt> <dd>

SoH 交換的唯一 [**StringCorrelationId**](nap-type-constants.md) 指標指標。

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
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





