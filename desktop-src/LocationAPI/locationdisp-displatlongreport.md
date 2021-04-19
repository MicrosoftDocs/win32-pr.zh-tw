---
description: 表示緯度/經度報表。
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: LocationDisp. DispLatLongReport 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976565"
---
# <a name="locationdispdisplatlongreport-object"></a>LocationDisp. DispLatLongReport 物件

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]

表示緯度/經度報表。

## <a name="members"></a>成員

**LocationDisp. DispLatLongReport** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**LocationDisp. DispLatLongReport** 物件具有這些屬性。



| 屬性                                                                         | 存取類型          | Description                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**高度**](locationdisp-displatlongreport-altitude.md)<br/>           | 唯讀<br/> | 目前的高度，以計量為單位。<br/>                                                                                                                                                           |
| [**AltitudeError**](locationdisp-displatlongreport-altitudeerror.md)<br/> | 唯讀<br/> | 高度錯誤，計量為。<br/>                                                                                                                                                             |
| [**ErrorRadius**](locationdisp-displatlongreport-errorradius.md)<br/>     | 唯讀<br/> | 從報告位置的距離（以計量為單位）。 此 radius 會與報告的位置合併為來源，並描述實際位置 proably 所在的圓形。<br/> |
| [**緯度**](locationdisp-displatlongreport-latitude.md)<br/>           | 唯讀<br/> | 目前的緯度（以度為單位）。<br/>                                                                                                                                                          |
| [**經度**](locationdisp-displatlongreport-longitude.md)<br/>         | 唯讀<br/> | 目前的經度（以度為單位）。<br/>                                                                                                                                                         |
| [**時間 戳**](locationdisp-displatlongreport-timestamp.md)<br/>         | 唯讀<br/> | 產生報表的日期和時間。<br/>                                                                                                                                       |



 

## <a name="remarks"></a>備註

您可以透過 [**LatLongReportFactory**](locationdisp-latlongreportfactory.md)物件的 [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md)屬性來取得這個物件。 您可以透過 [**NewLatLongReport**](newlatlongreport.md) 事件接收此物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

