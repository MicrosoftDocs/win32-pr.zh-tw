---
description: LocationDisp. DispLatLongReport. Timestamp 屬性-產生報表的日期和時間。
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: LocationDisp. DispLatLongReport. Timestamp 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 02b1d2bc344ec954f8c309e2370755464857fd754b16f6664760f9df4e0e5f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129908"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a>LocationDisp. DispLatLongReport. Timestamp 屬性

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows。裝置。地理位置**](/uwp/api/Windows.Devices.Geolocation)API。\]

產生報表的日期和時間。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a>屬性值

這個屬性是唯讀 **日期**。 時間戳記是以國際標準時間 (UTC) 提供。

## <a name="remarks"></a>備註

請注意，當您將時間戳記顯示為字串時，指令碼語言（例如 Microsoft JScript）可能會要求您執行轉換成其他時間格式。

## <a name="examples"></a>範例

如需如何使用這個屬性的範例，請參閱 [簡單的 LatLong 報表範例](/uwp/api/Windows.Devices.Geolocation)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

