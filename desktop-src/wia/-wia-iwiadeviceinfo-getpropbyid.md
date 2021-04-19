---
description: DeviceInfo 物件的 GetPropById 方法會使用裝置屬性的識別碼來傳回其值。
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: DeviceInfo. GetPropById 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001717"
---
# <a name="deviceinfogetpropbyid-method"></a><span data-ttu-id="045d3-103">DeviceInfo. GetPropById 方法</span><span class="sxs-lookup"><span data-stu-id="045d3-103">DeviceInfo.GetPropById method</span></span>

<span data-ttu-id="045d3-104">[**DeviceInfo**](-wia-deviceinfo.md)物件的 **GetPropById** 方法會使用裝置屬性的識別碼來傳回其值。</span><span class="sxs-lookup"><span data-stu-id="045d3-104">The **GetPropById** method of the [**DeviceInfo**](-wia-deviceinfo.md) object uses a device property's ID to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="045d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="045d3-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="045d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="045d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="045d3-107"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="045d3-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="045d3-108">類型： **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="045d3-108">Type: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span></span>

<span data-ttu-id="045d3-109">指定屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="045d3-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="045d3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="045d3-110">Return value</span></span>

<span data-ttu-id="045d3-111">類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="045d3-111">Type: **VARIANT**</span></span>

<span data-ttu-id="045d3-112">這個方法會傳回 *識別碼* 所指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="045d3-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="045d3-113">備註</span><span class="sxs-lookup"><span data-stu-id="045d3-113">Remarks</span></span>

<span data-ttu-id="045d3-114">您可以使用這個方法，從識別碼中找出裝置屬性的值。</span><span class="sxs-lookup"><span data-stu-id="045d3-114">Use this method to find the value of a device property from its ID.</span></span> <span data-ttu-id="045d3-115">如需屬性識別碼的清單，請參閱 [WIA 屬性常數定義](-wia-wia-property-constant-definitions.md)。</span><span class="sxs-lookup"><span data-stu-id="045d3-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="045d3-116">如需 Windows 映像取得 (WIA) 屬性本身的詳細資訊，請參閱 [Wia 屬性常數](-wia-wia-property-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="045d3-116">For information about Windows Image Acquisition (WIA) properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="045d3-117">若為 Microsoft Visual Basic 的應用程式，請新增「Windows 映像取得1.01 類型程式庫」的參考。</span><span class="sxs-lookup"><span data-stu-id="045d3-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="045d3-118">該檔案中定義的下列常數適用于此方法：</span><span class="sxs-lookup"><span data-stu-id="045d3-118">This following constants defined in that file are valid for this method:</span></span>

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a><span data-ttu-id="045d3-119">範例</span><span class="sxs-lookup"><span data-stu-id="045d3-119">Examples</span></span>

<span data-ttu-id="045d3-120">下列範例示範如何使用 **GetPropById** 方法來取得屬性值。</span><span class="sxs-lookup"><span data-stu-id="045d3-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="045d3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="045d3-121">Requirements</span></span>



| <span data-ttu-id="045d3-122">需求</span><span class="sxs-lookup"><span data-stu-id="045d3-122">Requirement</span></span> | <span data-ttu-id="045d3-123">值</span><span class="sxs-lookup"><span data-stu-id="045d3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="045d3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="045d3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="045d3-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="045d3-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="045d3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="045d3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="045d3-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="045d3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="045d3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="045d3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="045d3-129"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="045d3-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




