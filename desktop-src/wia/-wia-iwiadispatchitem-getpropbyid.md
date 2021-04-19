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
ms.openlocfilehash: 54eb329d51005893b89a9fd28f160ff616e682df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987548"
---
# <a name="itemgetpropbyid-method"></a><span data-ttu-id="3d2e8-103">GetPropById 方法</span><span class="sxs-lookup"><span data-stu-id="3d2e8-103">Item.GetPropById method</span></span>

<span data-ttu-id="3d2e8-104">[**Item**](-wia-item.md)物件的 **GetPropById** 方法會使用 item 屬性的 ID 來傳回其值。</span><span class="sxs-lookup"><span data-stu-id="3d2e8-104">The **GetPropById** method of the [**Item**](-wia-item.md) object uses the ID of an item property to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="3d2e8-105">Syntax</span></span>


```JScript
retVal = Item.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="3d2e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="3d2e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d2e8-107"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="3d2e8-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2e8-108">類型： **[WiaItemPropertyId](-wia-wiaitempropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="3d2e8-108">Type: **[WiaItemPropertyId](-wia-wiaitempropertyid.md)**</span></span>

<span data-ttu-id="3d2e8-109">指定屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d2e8-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d2e8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d2e8-110">Return value</span></span>

<span data-ttu-id="3d2e8-111">類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="3d2e8-111">Type: **VARIANT**</span></span>

<span data-ttu-id="3d2e8-112">這個方法會傳回 *識別碼* 所指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3d2e8-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2e8-113">備註</span><span class="sxs-lookup"><span data-stu-id="3d2e8-113">Remarks</span></span>

<span data-ttu-id="3d2e8-114">您可以使用這個方法，從識別碼中找出專案屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3d2e8-114">Use this method to find the value of an item property from its ID.</span></span> <span data-ttu-id="3d2e8-115">如需屬性識別碼的清單，請參閱 [WIA 屬性常數定義](-wia-wia-property-constant-definitions.md)。</span><span class="sxs-lookup"><span data-stu-id="3d2e8-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="3d2e8-116">如需屬性本身的詳細資訊，請參閱 [WIA 屬性常數](-wia-wia-property-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="3d2e8-116">For information about the properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="3d2e8-117">若為 Microsoft Visual Basic 的應用程式，請新增「Windows 映像取得1.01 類型程式庫」的參考。</span><span class="sxs-lookup"><span data-stu-id="3d2e8-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="3d2e8-118">在該檔案中定義的下列常數，只對 (裝置專案) 的根專案有效：</span><span class="sxs-lookup"><span data-stu-id="3d2e8-118">The following constants defined in that file are valid only for root items (device items):</span></span>

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

## <a name="examples"></a><span data-ttu-id="3d2e8-119">範例</span><span class="sxs-lookup"><span data-stu-id="3d2e8-119">Examples</span></span>

<span data-ttu-id="3d2e8-120">下列範例示範如何使用 **GetPropById** 方法來取得屬性值。</span><span class="sxs-lookup"><span data-stu-id="3d2e8-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3d2e8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d2e8-121">Requirements</span></span>



| <span data-ttu-id="3d2e8-122">需求</span><span class="sxs-lookup"><span data-stu-id="3d2e8-122">Requirement</span></span> | <span data-ttu-id="3d2e8-123">值</span><span class="sxs-lookup"><span data-stu-id="3d2e8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2e8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d2e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2e8-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d2e8-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d2e8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d2e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2e8-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d2e8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3d2e8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3d2e8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d2e8-129"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3d2e8-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




