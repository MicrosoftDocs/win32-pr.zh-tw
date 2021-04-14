---
title: 'INapSystemHealthAgentCallback NotifyOrphanedSoHRequest 方法 (NapSystemHealthAgent .h) '
description: 如果從 SHA 查詢了 SoHRequest，則會呼叫，但是回應絕不會傳回。
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- NotifyOrphanedSoHRequest 方法 NAP
- NotifyOrphanedSoHRequest 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，NotifyOrphanedSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385190"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>INapSystemHealthAgentCallback：： NotifyOrphanedSoHRequest 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

如果從 SHA 查詢 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則會呼叫 **INapSystemHealthAgentCallback：： NotifyOrphanedSoHRequest** 方法，但回應絕不會傳回。

## <a name="syntax"></a>語法


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*correlationId* \[在\]
</dt> <dd>

識別孤立 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)的唯一 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                          | Description                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 表示成功。<br/> |



 

## <a name="remarks"></a>備註

此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。

在下列情況下，系統可以呼叫這個方法：

-   無法在網路上傳送 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。
-   [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)是在網路上傳送，但未傳回 **SoHResponse** ，也就是 enforcer 超時，或伺服器端沒有對應的 SHV。
-   連接中斷或 enforcer 離線。

這只是最棒的通知，因此 Sha 不能依賴這項資訊來清除狀態。 在許多情況下，將不會收到 SHA 的通知：

-   如果是 enforcer misbehaves，也就是它不會在連接狀態為關閉時通知 SHA。
-   如果 enforcer 損毀。
-   在錯誤狀況中，也就是 NapAgent 記憶體不足。

Sha 可能會在第一次系結至 NapAgent 時收到一些偽造的通知，例如，當 SHA 系結時，如果 SoH 交換正在進行中，則會發生一些假的通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthAgent。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





