---
title: SystemMonitor. ChartScroll 屬性
description: 抓取或設定值，這個值會決定折線圖是否會在視圖中滾動。
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- ChartScroll 屬性 SysMon
- ChartScroll 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，ChartScroll 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934478"
---
# <a name="systemmonitorchartscroll-property"></a>SystemMonitor. ChartScroll 屬性

抓取或設定值，這個值會決定折線圖是否會在視圖中滾動。

## <a name="syntax"></a>Syntax


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a>屬性值

如果折線圖會從右至左連續滾動，則為 True;否則，如果折線圖是由左至右繪製，並在視圖中換行，則為 False。 預設值為 False。

## <a name="remarks"></a>備註

如果 [**SystemMonitor**](systemmonitor-displaytype.md) 不是 [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)，則會忽略此值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





