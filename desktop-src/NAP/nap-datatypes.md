---
title: 'NAP 資料類型 (NapTypes .h) '
description: 請注意，從 Windows 10 網路存取保護的資料類型 (NAP) API 之後，就無法使用網路存取保護平臺，如下所示。
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- 百分比
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934874"
---
# <a name="nap-datatypes"></a>NAP 資料類型

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

網路存取保護 (NAP) API 的資料類型如下所示。


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

**ProbationTime**
</dt> <dd>

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構，包含與用戶端電腦的試用期相關的時間。

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

值，指定 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包的最大大小（以位元組為單位）的可能值範圍，如範圍 ([**minProtocolMaxSize，maxProtocolMaxSize**](nap-type-constants.md)) 的定義。

</dd> <dt>

**NapComponentId**
</dt> <dd>

Sha、Shv 和強制用戶端用來識別本身的唯一4位元組識別碼。 前三個位元組是供應商的 IETF 指派 SMI-S 碼，最後一個位元組會識別元件本身。

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

用來識別 SHA/SHV 配對的 **NapComponentId** 值。

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

用來識別強制用戶端的 **NapComponentId** 值。

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

值，這個值會指定要 [**maxSystemHealthEntityCount**](nap-type-constants.md)的) 範圍 0 (零零的 NAP 系統中已註冊的 sha 數目。

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

值，指定 NAP 系統中的強制用戶端數目，範圍介於 0 (零) [**maxEnforcerCount**](nap-type-constants.md)。

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

用來將 [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh)配對至 **SoHResponses** 之 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)結構的 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)版本。

</dd> <dt>

**ConnectionId**
</dt> <dd>

唯一的全域唯一識別碼 (GUID) 用來識別強制用戶端所維護的 NAP 連接。

</dd> <dt>

**百分比**
</dt> <dd>

值，其中包含 0 (零) 的百分比，以及已完成的補救措施100

</dd> <dt>

**MessageId**
</dt> <dd>

用來識別 NAP 系統訊息的唯一值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                                                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                                                                                |
| 標頭<br/>                   | <dl> <dt>NapTypes .h;</dt><dt>NapEnforcementClient .h</dt> </dl> |



 

