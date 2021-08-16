---
title: SystemMonitor. MaximumScale 屬性
description: 抓取或設定圖形垂直 (Y) 軸的最大值。
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- MaximumScale 屬性 SysMon
- MaximumScale 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，MaximumScale 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 176ebab3b2879b3d158310ec61fa9e65df45f8b502029ede1c58c2c1dd33f225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882027"
---
# <a name="systemmonitormaximumscale-property"></a>SystemMonitor. MaximumScale 屬性

抓取或設定圖形垂直 (Y) 軸的最大值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a>屬性值

圖形垂直軸的正面最大值。 垂直尺規的預設最大值為100。 最小值，您可以將最大值設為一個以上的值，而不是 [**MinimumScale**](systemmonitor-minimumscale.md) 值。 您可以將最大值設定為999999999的最大值。

## <a name="remarks"></a>備註

控制項會根據顯示控制項的大小，自動調整顯示在垂直尺規上的尺規數位位置。

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

[**SystemMonitor.MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





