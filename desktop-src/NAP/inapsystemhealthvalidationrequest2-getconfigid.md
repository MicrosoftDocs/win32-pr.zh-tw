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
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967764"
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



| 傳回碼                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業成功。<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | ConfigID 參數為 **Null**。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





