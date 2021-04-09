---
title: SystemMonitor. ReportValueType 屬性
description: 抓取或設定值，這個值會決定長條圖和報表檢視是否會圖形化取樣間隔期間所取樣的最後一個值，或取樣中的計算值，例如平均或最小計數器值。
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- ReportValueType 屬性 SysMon
- ReportValueType 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，ReportValueType 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934334"
---
# <a name="systemmonitorreportvaluetype-property"></a>SystemMonitor. ReportValueType 屬性

抓取或設定值，這個值會決定長條圖和報表檢視是否會圖形化取樣間隔期間所取樣的最後一個值，或取樣中的計算值，例如平均或最小計數器值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>屬性值

判斷長條圖和報表檢視是否會在取樣間隔期間，或取樣間隔中的計算值，繪製出最後取樣的值。 如需可能的值，請參閱 [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants)。

## <a name="remarks"></a>備註

如果 [**SystemMonitor**](systemmonitor-displaytype.md)未 [**DisplayTypeConstants.sysMonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)或 **DisplayTypeConstants.sysmonReport**，SYSMON 會忽略此值，並使用 [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) 。

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

 

 





