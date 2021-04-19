---
title: SystemMonitor. ShowTimeAxisLabels 屬性
description: 抓取或設定值，這個值會判斷圖形視圖的水準 (X) 軸是否包含標籤。
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- ShowTimeAxisLabels 屬性 SysMon
- ShowTimeAxisLabels 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，ShowTimeAxisLabels 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965891"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a>SystemMonitor. ShowTimeAxisLabels 屬性

抓取或設定值，這個值會判斷圖形視圖的水準 (X) 軸是否包含標籤。

## <a name="syntax"></a>Syntax


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a>屬性值

True 值會將標籤套用至 X 軸。 False 的值將不會。 預設值是 False。

## <a name="remarks"></a>備註

SYSMON 會忽略橫條圖、報表和長條圖的這個屬性。

針對折線圖，SYSMON 會使用取樣計數器值作為標籤的時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





