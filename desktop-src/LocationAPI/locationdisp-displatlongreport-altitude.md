---
description: 目前的高度，以計量為單位。 高度相對於參考橢圓體。
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp. DispLatLongReport. 海拔屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8ee6c2cd4257d7f7db97b89a5af4603f5c5129b7f07fe9bfbe6444bb9d347422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067938"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>LocationDisp. DispLatLongReport. 海拔屬性

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows。裝置。地理位置**](/uwp/api/Windows.Devices.Geolocation)API。\]

目前的高度，以計量為單位。 高度相對於參考橢圓體。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>屬性值

這個屬性是唯讀的 (雙精確度浮點數) 的 **數位** 。

## <a name="remarks"></a>備註

不需要定位感應器來提供此屬性。 您應該在嘗試存取此屬性時處理例外狀況。

**高度** 方法會抓取 Geodetic 系統 (WGS 84) 的最新修訂所定義之參考橢圓體的高度，而不是相對於海平面的高度。

## <a name="examples"></a>範例

如需如何使用這個屬性的範例，請參閱 [簡單的 LatLong 報表範例](/uwp/api/Windows.Devices.Geolocation)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

