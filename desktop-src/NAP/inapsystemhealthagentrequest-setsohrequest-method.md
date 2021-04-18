---
title: 'INapSystemHealthAgentRequest SetSoHRequest 方法 (NapSystemHealthAgent .h) '
description: 健康情況代理程式會使用它來寫入自呼叫 INapSystemHealthAgentCallback GetSoHRequest 所產生的 SoH 要求。
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- SetSoHRequest 方法 NAP
- SetSoHRequest 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，SetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968954"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a>INapSystemHealthAgentRequest：： SetSoHRequest 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

健康情況代理程式會使用 **INapSystemHealthAgentRequest：： SetSoHRequest** 方法，來寫入由呼叫 [**INapSystemHealthAgentCallback：： GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)所產生的 SoH 要求。

## <a name="syntax"></a>語法


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*sohRequest* \[在\]
</dt> <dd>

[**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)封包的指標。

</dd> <dt>

*cacheSohForLaterUse* \[在\]
</dt> <dd>

如果 NapAgent 應該快取 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林****值為 TRUE** ，否則為 **FALSE** 。

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

 

 





