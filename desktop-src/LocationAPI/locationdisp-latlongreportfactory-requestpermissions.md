---
description: 開啟 [系統] 對話方塊來要求啟用位置之裝置的使用者權限。
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: LocationDisp. LatLongReportFactory. RequestPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed789aca4b6c9d0db50a3e7b6cae33d55d22920c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989471"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>LocationDisp. LatLongReportFactory. RequestPermissions 方法

\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。 若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]

開啟 [系統] 對話方塊來要求啟用位置之裝置的使用者權限。

## <a name="syntax"></a>語法


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* 
</dt> <dd>

不使用此參數，應該設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

呼叫是同步的，且呼叫端會等候對話方塊關閉。

> [!Note]  
> 如果以受保護模式執行的應用程式（例如瀏覽器協助程式物件） (BHO) 用於 Internet Explorer，則會呼叫 **RequestPermissions**，而使用者在對話方塊中選擇 [ **不要啟用此定位感應器** ] 選項，將不會啟用位置提供者，但是如果相同的使用者再次呼叫 **RequestPermissions** ，則 Windows 會再次顯示此對話方塊。 在受保護模式下執行的應用程式，可能會選擇不在啟動時呼叫 **RequestPermissions** ，讓使用者不會在每次應用程式啟動時看到可能的不必要對話方塊。

 

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱 [接聽 LatLong 報表事件](/uwp/api/Windows.Devices.Geolocation)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                  |



 

