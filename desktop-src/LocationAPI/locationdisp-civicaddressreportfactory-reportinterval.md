---
description: 目前的市政位址報告事件間隔（以毫秒為單位）。
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: LocationDisp. CivicAddressReportFactory. ReportInterval 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: d18db71ac97bbfca60d4892bb151388eee97dbb481508b86b595d5dda74954fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387159"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>LocationDisp. CivicAddressReportFactory. ReportInterval 屬性

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows。裝置。地理位置**](/uwp/api/Windows.Devices.Geolocation)API。\]

目前的市政位址報告事件間隔（以毫秒為單位）。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>屬性值

這個屬性是讀取/寫入的 **ULONG**。

## <a name="remarks"></a>備註

此值是位置提供者的要求。 位置提供者不需要在您要求的間隔提供報告。 讀取這個屬性的值，以探索真正的報表間隔設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

