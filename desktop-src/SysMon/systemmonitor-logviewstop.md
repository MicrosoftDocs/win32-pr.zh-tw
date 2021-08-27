---
title: SystemMonitor. LogViewStop 屬性
description: 取得或設定用來從記錄檔抓取計數器值的結束日期。
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- LogViewStop 屬性 SysMon
- LogViewStop 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，LogViewStop 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c30305f99e0d9bf66dd0f00dccc7674073e0f7058bca4284411c9d24426b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882072"
---
# <a name="systemmonitorlogviewstop-property"></a>SystemMonitor. LogViewStop 屬性

取得或設定用來從記錄檔抓取計數器值的結束日期。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>屬性值

用來從記錄檔中取出計數器值的結束日期。

## <a name="remarks"></a>備註

SYSMON 會從 [**SystemMonitor LogViewStart**](systemmonitor-logviewstart.md) 和停止日期中的記錄檔抓取計數器值（含）。

如果您未指定停止值，或將此屬性設定為晚于記錄檔中所包含之最後一個日期的日期值，則 SYSMON 會將此值變更為在記錄檔中找到的最新日期值。

如果這個屬性設定為小於 [**LogViewStart**](systemmonitor-logviewstart.md)的日期值，則 SYSMON 會將值變更為 **LogViewStart** 的值。

您必須在設定停止日期之前設定開始日期;否則，這兩個值會設定為 MinValue，如果您在設定 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)之後設定日期，則只會從記錄檔中取出第一個計數器值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor.LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





