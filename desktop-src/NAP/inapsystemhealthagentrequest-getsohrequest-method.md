---
title: 'INapSystemHealthAgentRequest GetSoHRequest 方法 (NapSystemHealthAgent .h) '
description: 可由 NapAgent 先前快取的 Sha get Soh 使用。
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025422"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>INapSystemHealthAgentRequest：： GetSoHRequest 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentRequest：： GetSoHRequest** 方法可以由 NapAgent 先前快取的 Sha get soh 使用。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sohRequest* \[擴展\]
</dt> <dd>

指向 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                            | Description                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                  | 作業成功。<br/>                                        |
| <dl> <dt>**NAP \_ E 沒有快取的 \_ \_ \_ SOH**</dt> </dl> | 找不到 SoH;NapAgent 沒有快取的複本。<br/> |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>        | 許可權錯誤，拒絕存取。<br/>                           |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>         | 系統資源限制，無法執行操作。<br/>     |



 

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

 

 





