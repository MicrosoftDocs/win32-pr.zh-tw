---
description: LocationDisp. CivicAddressReportFactory。 Status 屬性-目前的報告狀態。
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: LocationDisp. CivicAddressReportFactory. Status 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8ba7d9e26a9741f80caed84d2a4ee4198eae05736aa8dee91019452cc3345ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693118"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>LocationDisp. CivicAddressReportFactory. Status 屬性

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows。裝置。地理位置**](/uwp/api/Windows.Devices.Geolocation)API。\]

目前的報表狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a>屬性值

這個屬性是唯讀的 (不帶正負 **號** 的長) 。



| 狀態                                                                                               | 意義                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | 不支援報表。<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | 錯誤。<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | 拒絕存取。<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | 正在初始化。<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 執行中。<br/>              |



 

## <a name="examples"></a>範例

如需如何使用這個屬性的範例，請參閱 [接聽市政位址報表事件](/uwp/api/Windows.Devices.Geolocation)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

