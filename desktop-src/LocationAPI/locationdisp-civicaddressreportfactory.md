---
description: 管理市政位址報表。
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: LocationDisp. CivicAddressReportFactory 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694160"
---
# <a name="locationdispcivicaddressreportfactory-object"></a>LocationDisp. CivicAddressReportFactory 物件

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]

管理市政位址報表。

## <a name="members"></a>成員

**LocationDisp. CivicAddressReportFactory** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**LocationDisp. CivicAddressReportFactory** 物件有這些方法。



| 方法                                                                                            | 描述                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-civicaddressreportfactory-listenforreports.md)               | 要求市政位址報告事件。<br/>                                              |
| [**RequestPermissions**](locationdisp-civicaddressreportfactory-requestpermissions.md)           | 開啟 [系統] 對話方塊來要求啟用位置之裝置的使用者權限。<br/> |
| [**StopListeningForReports**](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | 取消市政位址報告事件要求。<br/>                                       |



 

### <a name="properties"></a>屬性

**LocationDisp. CivicAddressReportFactory** 物件具有這些屬性。



| 屬性                                                                                        | 存取類型           | Description                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | 唯讀<br/>  | 目前的 [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md)。<br/> |
| [**DesiredAccuracy**](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | 讀取/寫入<br/> | 目前的預期精確度設定。<br/>                                                           |
| [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | 讀取/寫入<br/> | 目前的市政位址報告事件間隔（以毫秒為單位）。<br/>                                |
| [**狀態**](locationdisp-civicaddressreportfactory-status.md)<br/>                      | 唯讀<br/>  | 目前的報表狀態。<br/>                                                                      |



 

## <a name="examples"></a>範例

下列範例程式碼示範如何在 HTML 程式碼中建立這個物件。


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



下列範例程式碼示範如何使用 Windows Script Host 在 JScript 中建立這個物件。


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



下列範例程式碼示範如何使用 Windows Script Host 在 VBScript 中建立這個物件。


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LocationDisp.CivicAddressReport**](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

