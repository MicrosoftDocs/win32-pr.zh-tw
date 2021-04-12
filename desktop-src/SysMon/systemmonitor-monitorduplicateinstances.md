---
title: SystemMonitor. MonitorDuplicateInstances 屬性
description: 抓取或設定值，這個值會決定是否可以監視計數器的多個實例。
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- MonitorDuplicateInstances 屬性 SysMon
- MonitorDuplicateInstances 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，MonitorDuplicateInstances 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384454"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a>SystemMonitor. MonitorDuplicateInstances 屬性

抓取或設定值，這個值會決定是否可以監視計數器的多個實例。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a>屬性值

True 表示可以監視計數器的多個實例， (True 是預設) 。 False 表示只能監視一個計數器的實例。

## <a name="remarks"></a>備註

\#如果有多個實例，則系統監視器會將 n 附加至每個實例名稱，但第一個名稱除外。 序號（n）會以1開始，並為每個新的實例遞增一。 例如，如果您指定「 \\ 處理 (\*) \\ % 處理器時間」，則計數器集合應該包含 svchost 的多個實例。 第一次出現的是 svchost，下一次出現的是 svchost \# 1，依此類推。

只有當您使用萬用字元 (\*) 作為實例名稱時，才會監視重複的實例。 如果您指定「 \\ 進程 (svchost) \\ % 處理器時間」，則只會監視找到的 svchost 第一個實例，而不是所有 svchost 實例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





