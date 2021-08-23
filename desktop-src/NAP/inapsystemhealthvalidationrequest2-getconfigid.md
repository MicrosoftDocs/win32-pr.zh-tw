---
title: 'INapSystemHealthValidationRequest2 GetConfigID 方法 (NapSystemHealthValidator .h) '
description: 系統健康狀態驗證 (Shv) 用來在驗證要求中取出設定識別碼。
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- GetConfigID 方法 NAP
- GetConfigID 方法 NAP，INapSystemHealthValidationRequest2 介面
- INapSystemHealthValidationRequest2 介面 NAP，GetConfigID 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72acdd170726d2d94e4fbc46864a7e5aab6b902d7b1ee25b63ee0fa9e376c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625978"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>INapSystemHealthValidationRequest2：： GetConfigID 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidationRequest2：： GetConfigId** 方法是由系統健康狀態驗證 (shv) 用來在驗證要求中取出設定識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*configID* \[擴展\]
</dt> <dd>

傳回時為 UINT32 的指標，其中包含 SHV 的設定識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                  | 描述                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業成功。<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | ConfigID 參數為 **Null**。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





