---
description: 從報告位置的距離（以計量為單位）。 此 radius 會與報告的位置結合為來源，以描述實際位置可能所在的圓形。
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: LocationDisp. DispLatLongReport. ErrorRadius 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988855"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a>LocationDisp. DispLatLongReport. ErrorRadius 屬性

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]

從報告位置的距離（以計量為單位）。 此 radius 會與報告的位置結合為來源，以描述實際位置可能所在的圓形。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a>屬性值

這個屬性是唯讀的 (雙精確度浮點數) 的 **數位** 。

## <a name="examples"></a>範例

如需如何使用這個屬性的範例，請參閱 [簡單的 LatLong 報表範例](/uwp/api/Windows.Devices.Geolocation)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

