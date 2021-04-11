---
title: 'INapSystemHealthAgentRequest GetSoHResponse 方法 (NapSystemHealthAgent .h) '
description: 當 NapAgent 呼叫 INapSystemHealthAgentCallback ProcessSoHResponse 時，health 代理程式會使用它來取得其 SoHResponse blob。
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- GetSoHResponse 方法 NAP
- GetSoHResponse 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetSoHResponse 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094243"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a>INapSystemHealthAgentRequest：： GetSoHResponse 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentRequest：： GetSoHResponse** 方法是由健康情況代理程式在 NapAgent 呼叫 [**INapSystemHealthAgentCallback：:P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md)時，用來取得其 SoHResponse blob。

## <a name="syntax"></a>語法


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sohResponse* \[擴展\]
</dt> <dd>

指向 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包指標的指標。

</dd> <dt>

*旗標* \[擴展\]
</dt> <dd>

旗標的指標，如果設定 [**shaFixup**](nap-type-constants.md) 位，則會啟用 SHA 的修正，否則會停用修正。



| 可能的值                                                                                                                                                          | 意義                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <dt>**shaFixup**</dt> </dl> | SHA 預期會根據回應來執行修復。 如果未設定此旗標，則即使 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 指出其狀況不良，SHA 仍不應執行修正。<br/> |



 

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

 

 





