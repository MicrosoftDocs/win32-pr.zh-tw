---
description: 管理緯度/經度報表。
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: LocationDisp. LatLongReportFactory 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852776"
---
# <a name="locationdisplatlongreportfactory-object"></a>LocationDisp. LatLongReportFactory 物件

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]

管理緯度/經度報表。

## <a name="members"></a>成員

**LocationDisp. LatLongReportFactory** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**LocationDisp. LatLongReportFactory** 物件有這些方法。



| 方法                                                                                       | 描述                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-latlongreportfactory-listenforreports.md)               | 要求緯度/經度報表事件。<br/>                                         |
| [**RequestPermissions**](locationdisp-latlongreportfactory-requestpermissions.md)           | 開啟 [系統] 對話方塊來要求啟用位置之裝置的使用者權限。<br/> |
| [**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85)) | 取消緯度/經度報表事件的要求。<br/>                             |



 

### <a name="properties"></a>屬性

**LocationDisp. LatLongReportFactory** 物件具有這些屬性。



| 屬性                                                                                | 存取類型           | Description                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**DesiredAccuracy**](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | 讀取/寫入<br/> | 目前的預期精確度值。<br/>                                                   |
| [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | 唯讀<br/>  | 目前的 [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)。<br/> |
| [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | 讀取/寫入<br/> | 目前的緯度/經度報表事件間隔（以毫秒為單位）。<br/>                 |
| [**狀態**](locationdisp-latlongreportfactory-status.md)<br/>                   | 唯讀<br/>  | 目前的報表狀態。<br/>                                                            |



 

## <a name="examples"></a>範例

下列範例程式碼示範如何在 HTML 程式碼中建立這個物件。


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



下列範例程式碼示範如何使用 Windows Script Host 在 JScript 中建立這個物件。


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



下列範例程式碼示範如何使用 Windows Script Host 在 VBScript 中建立這個物件。


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md)
</dt> </dl>

 

