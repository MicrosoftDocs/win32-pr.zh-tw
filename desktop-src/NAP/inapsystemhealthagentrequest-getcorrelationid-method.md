---
title: 'INapSystemHealthAgentRequest GetCorrelationId 方法 (NapSystemHealthAgent .h) '
description: 系統健康狀態代理程式會使用它來相互關聯 SoH 的和 SoH 回應。
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- GetCorrelationId 方法 NAP
- GetCorrelationId 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetCorrelationId 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509480"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a>INapSystemHealthAgentRequest：： GetCorrelationId 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

系統健康狀態代理程式會使用 **INapSystemHealthAgentRequest：： GetCorrelationId** 方法，將 SoH 和 soh 回應相互關聯。

## <a name="syntax"></a>語法


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*correlationId* \[擴展\]
</dt> <dd>

SoH 交換的唯一 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) 指標。

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
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





