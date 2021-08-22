---
title: SystemMonitor. EnableDigitGrouping 屬性
description: 抓取或設定值，這個值會決定 SYSMON 是否在顯示數值時使用數位群組。
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- EnableDigitGrouping 屬性 SysMon
- EnableDigitGrouping 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，EnableDigitGrouping 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d910e479cc0a957ea5f1332d7fead0f93badd797bfe2d90b26f9914f0c3d863a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882603"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>SystemMonitor. EnableDigitGrouping 屬性

抓取或設定值，這個值會決定 SYSMON 是否在顯示數值時使用數位群組。

## <a name="syntax"></a>Syntax


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>屬性值

若為 True，SYSMON 會在顯示數值時分組位數，例如1214。 如果為 False，則不會將數值分組，例如1214。 預設值為 True。

## <a name="remarks"></a>備註

數位群組符號已當地語系化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





