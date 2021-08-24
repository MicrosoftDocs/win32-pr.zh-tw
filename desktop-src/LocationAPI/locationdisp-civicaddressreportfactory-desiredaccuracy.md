---
description: LocationDisp. CivicAddressReportFactory. DesiredAccuracy 屬性-目前的預期精確度值。
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: LocationDisp. CivicAddressReportFactory. DesiredAccuracy 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca2d4f4a7be4afa800cfe81b5df7396be579197e7f997019f4ece3a39598c975
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693128"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a>LocationDisp. CivicAddressReportFactory. DesiredAccuracy 屬性

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows。裝置。地理位置**](/uwp/api/Windows.Devices.Geolocation)API。\]

目前的預期精確度值。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>屬性值

這個屬性是讀取/寫入的 **ULONG**。



| 值                                                                        | 意義                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 預設值。 感應器應使用可優化電源使用的精確度，以及其他成本考慮。<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | 感應器應該盡可能提供最精確的報告。 這包括使用可能須付費的服務，或是耗用更多的電池電力或是連線頻寬。<br/> |



 

## <a name="remarks"></a>備註

此值是對位置提供者的要求。 不需要位置提供者來提供您要求的精確度。 讀取此屬性的值，以探索真正的精確度設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

