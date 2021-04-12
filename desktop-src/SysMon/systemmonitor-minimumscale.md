---
title: SystemMonitor. MinimumScale 屬性
description: 抓取或設定圖形垂直 (Y) 軸的最小值。
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- MinimumScale 屬性 SysMon
- MinimumScale 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，MinimumScale 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465213"
---
# <a name="systemmonitorminimumscale-property"></a>SystemMonitor. MinimumScale 屬性

抓取或設定圖形垂直 (Y) 軸的最小值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a>屬性值

圖形垂直軸的正面最小值。 垂直尺規的預設最小值是0。 您可以將最小值設為一個小於 [**MaximumScale**](systemmonitor-maximumscale.md) 值的最大值。

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

[**SystemMonitor.MaximumScale**](systemmonitor-maximumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





