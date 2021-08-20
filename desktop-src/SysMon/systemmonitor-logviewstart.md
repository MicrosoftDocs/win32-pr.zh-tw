---
title: SystemMonitor. LogViewStart 屬性
description: 取得或設定用來從記錄檔抓取計數器值的開始日期。
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- LogViewStart 屬性 SysMon
- LogViewStart 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，LogViewStart 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc1c7c4a46ac746582d62ee7ce08980b078eb8d972cb6b4d3ed787b49f2285f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955401"
---
# <a name="systemmonitorlogviewstart-property"></a>SystemMonitor. LogViewStart 屬性

取得或設定用來從記錄檔抓取計數器值的開始日期。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a>屬性值

用來從記錄檔中取出計數器值的開始日期。

## <a name="remarks"></a>備註

SYSMON 會從開始和 SystemMonitor 中的記錄檔抓取計數器值（含） [**。**](systemmonitor-logviewstop.md)

如果您沒有指定開始日期，或是將這個屬性設定為在記錄檔中找到之日期值範圍以外的日期值，SYSMON 會將值變更為記錄檔中找到的最早日期值。

如果這個屬性設定為大於 [**LogViewStop**](systemmonitor-logviewstop.md)的日期值，則 SYSMON 會將值變更為 **LogViewStop** 的值。

如果您指定開始和停止日期，則應該在設定 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)之前指定日期。

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

[**SystemMonitor**](systemmonitor-logfiles.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





