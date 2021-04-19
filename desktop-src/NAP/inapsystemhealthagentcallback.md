---
title: 'INapSystemHealthAgentCallback 介面 (NapSystemHealthAgent .h) '
description: 由系統宣告並由 SHA 寫入器所執行，讓 NapAgent 可以與 SHA 進行通訊。
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- INapSystemHealthAgentCallback 介面 NAP
- INapSystemHealthAgentCallback 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969196"
---
# <a name="inapsystemhealthagentcallback-interface"></a>INapSystemHealthAgentCallback 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthAgentCallback** 介面會提供由系統宣告並由 sha 寫入器所執行的回呼方法，讓 NapAgent 可以與 sha 進行通訊。

## <a name="members"></a>成員

**INapSystemHealthAgentCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapSystemHealthAgentCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapSystemHealthAgentCallback** 介面具有這些方法。



| 方法                                                                                                                                           | 描述                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentCallback::CompareSoHRequests**](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | 由 SHA 用來比較 Soh。<br/>                                                                      |
| [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | 由 NapAgent 呼叫以判斷 SHA 的狀態。<br/>                                                 |
| [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | 由 NapAgent 呼叫以查詢 SHA 的 SoH 要求。<br/>                                                    |
| [**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | 如果從 SHA 查詢 SoH 要求，但回應從未回傳，則呼叫。<br/>                      |
| [**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | 由 NapAgent 呼叫，表示系統隔離狀態或試用結束時間已變更。<br/> |
| [**INapSystemHealthAgentCallback：:P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md)                             | 當 NapAgent 收到目的地為此健康情況代理程式的 SoH 回應時呼叫。<br/>                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

