---
description: Item 物件的 GetPropById 方法會使用 item 屬性的 ID 來傳回其值。
ms.assetid: 00f7a91c-fd55-4016-a932-f710045a14b8
title: GetPropById 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 5c8d5f68114f74505fce11ca8872370a802e31400159146d7030ec34339c7d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208372"
---
# <a name="itemgetpropbyid-method"></a>GetPropById 方法

[**Item**](-wia-item.md)物件的 **GetPropById** 方法會使用 item 屬性的 ID 來傳回其值。

## <a name="syntax"></a>語法


```JScript
retVal = Item.GetPropById(
  Id
)
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

類型： **[WiaItemPropertyId](-wia-wiaitempropertyid.md)**

指定屬性的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **VARIANT**

這個方法會傳回 *識別碼* 所指定之屬性的值。

## <a name="remarks"></a>備註

您可以使用這個方法，從識別碼中找出專案屬性的值。 如需屬性識別碼的清單，請參閱 [WIA 屬性常數定義](-wia-wia-property-constant-definitions.md)。 如需屬性本身的詳細資訊，請參閱 [WIA 屬性常數](-wia-wia-property-constants.md)。

針對 Microsoft Visual Basic 的應用程式，請新增「Windows 影像取得1.01 型別程式庫」的參考。 在該檔案中定義的下列常數，只對 (裝置專案) 的根專案有效：

``` syntax
const FirmwareVersion = 1026
const ConnectStatus = 1027
const DeviceTime = 1028
const PicturesTaken = 2050
const PicturesRemaining = 2051
const ExposureMode = 2052
const ExposureCompensation = 2053
const ExposureTime = 2054
const FNumber = 2055
const FlashMode = 2056
const FocusMode = 2057
const FocusManualDist = 2058
const ZoomPosition = 2059
const PanPosition = 2060
const TiltPostion = 2061
const TimerMode = 2062
const TimerValue = 2063
const PowerMode = 2064
const BatteryStatus = 2065
const Dimension = 2070
const HorizontalBedSize = 3074
const VerticalBedSize = 3075
const HorizontalSheetFeedSize = 3076
const VerticalSheetFeedSize = 3077
const SheetFeederRegistration = 3078
const HorizontalBedRegistration = 3079
const VerticalBedRegistraion = 3080
const PlatenColor = 3081
const PadColor = 3082
const FilterSelect = 3083
const DitherSelect = 3084
const DitherPatternData = 3085
const DocumentHandlingCapabilities = 3086
const DocumentHandlingStatus = 3087
const DocumentHandlingSelect = 3088
const DocumentHandlingCapacity = 3089
const HorizontalOpticalResolution = 3090
const VerticalOpticalResolution = 3091
const EndorserCharacters = 3092
const EndorserString = 3093
const ScanAheadPages = 3094
const MaxScanTime = 3095
const Pages = 3096
const PageSize = 3097
const PageWidth = 3098
const PageHeight = 3099
const Preview = 3100
const TransparencyAdapter = 3101
const TransparecnyAdapterSelect = 3102
```

## <a name="examples"></a>範例

下列範例示範如何使用 **GetPropById** 方法來取得屬性值。


```JScript
<SCRIPT LANGUAGE="VBScript">
const DeviceType = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    objRootItem=objDeviceInfo.Create()
    objSelectedItems=objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItem
    PropValue = objItem.GetPropById(DeviceType)
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |



 

 




