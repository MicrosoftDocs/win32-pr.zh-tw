---
title: SystemMonitor. DataPointCount 屬性
description: 抓取或設定線條圖形中顯示的資料點數目。
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- DataPointCount 屬性 SysMon
- DataPointCount 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，DataPointCount 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934147"
---
# <a name="systemmonitordatapointcount-property"></a>SystemMonitor. DataPointCount 屬性

抓取或設定線條圖形中顯示的資料點數目。

## <a name="syntax"></a>Syntax


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a>屬性值

折線圖中顯示的資料點數目。 預設值為100資料點。 值的有效範圍是2到1000。

## <a name="remarks"></a>備註

只有在 [**SystemMonitor DataSourceType**](systemmonitor-datasourcetype.md) 為 **sysmonCurrentActivity** 時，才會使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





