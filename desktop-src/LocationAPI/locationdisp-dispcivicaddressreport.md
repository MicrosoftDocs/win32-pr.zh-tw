---
description: 代表市政位址報表。
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: LocationDisp. DispCivicAddressReport 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5646bd6df1a2523faf481bc867acc67dbd0a647b4cdf3f033d7327a66174d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129978"
---
# <a name="locationdispdispcivicaddressreport-object"></a>LocationDisp. DispCivicAddressReport 物件

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows。裝置。地理位置**](/uwp/api/Windows.Devices.Geolocation)API。\]

代表市政位址報表。

## <a name="members"></a>成員

**LocationDisp. DispCivicAddressReport** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**LocationDisp. DispCivicAddressReport** 物件具有這些屬性。



| 屬性                                                                              | 存取類型          | 描述                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | 唯讀<br/> | 街道位址的第一行。<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | 唯讀<br/> | 街道位址的第二行。<br/>             |
| [**City**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | 唯讀<br/> | 城市名稱。<br/>                                   |
| [**/**](locationdisp-civicaddressreport-countryregion.md)<br/>     | 唯讀<br/> | 國家或地區名稱。<br/>                      |
| [**DetailLevel**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | 唯讀<br/> | 報表的詳細層級。<br/>                 |
| [**郵遞區號**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | 唯讀<br/> | 郵遞區號。<br/>                                 |
| [**StateProvince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | 唯讀<br/> | 省份名稱。<br/>                      |
| [**時間 戳**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | 唯讀<br/> | 產生報表的日期和時間。<br/> |



 

## <a name="remarks"></a>備註

您可以透過 [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md)物件的 [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md)屬性來取得這個物件。 您可以透過 [**NewCivicAddressReport**](newcivicaddressreport.md) 事件接收此物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

