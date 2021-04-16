---
description: Wia 物件的 Create 方法會連接到指定的 Windows 映像取得 (WIA) 裝置，並傳回代表該裝置的專案物件。
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Wia. 建立方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513428"
---
# <a name="wiacreate-method"></a><span data-ttu-id="fb48e-103">Wia. 建立方法</span><span class="sxs-lookup"><span data-stu-id="fb48e-103">Wia.Create method</span></span>

<span data-ttu-id="fb48e-104">[**Wia**](-wia-wia.md)物件的 **Create** 方法會連接到指定的 WINDOWS 映射取得 (Wia) 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。</span><span class="sxs-lookup"><span data-stu-id="fb48e-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb48e-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb48e-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="fb48e-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb48e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb48e-107">*裝置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb48e-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb48e-108">類型： \**VARIANT \** _</span><span class="sxs-lookup"><span data-stu-id="fb48e-108">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="fb48e-109">指定要連接的 WIA 裝置。</span><span class="sxs-lookup"><span data-stu-id="fb48e-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb48e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb48e-110">Return value</span></span>

<span data-ttu-id="fb48e-111">類型： _ *IWiaDispatchItem*\*</span><span class="sxs-lookup"><span data-stu-id="fb48e-111">Type: _ *IWiaDispatchItem*\*</span></span>

<span data-ttu-id="fb48e-112">如果成功，這個方法會傳回代表 WIA 硬體裝置 (根專案) 的 [**專案**](-wia-item.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="fb48e-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb48e-113">備註</span><span class="sxs-lookup"><span data-stu-id="fb48e-113">Remarks</span></span>

<span data-ttu-id="fb48e-114">*Device* 參數會指定 [**DeviceInfo**](-wia-deviceinfo.md)物件，方法是傳遞物件本身、其在集合物件中的索引，或其 [**Id**](-wia-iwiadeviceinfo-id.md)屬性的值。</span><span class="sxs-lookup"><span data-stu-id="fb48e-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="fb48e-115">傳遞 **Nothing** 以顯示允許使用者選取裝置的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fb48e-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="fb48e-116">範例</span><span class="sxs-lookup"><span data-stu-id="fb48e-116">Examples</span></span>

<span data-ttu-id="fb48e-117">下列 VBScript 範例示範如何使用 **Create** 方法。</span><span class="sxs-lookup"><span data-stu-id="fb48e-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="fb48e-118">第一個範例會將 [**DeviceInfo**](-wia-deviceinfo.md) 物件傳遞至 **Create** 方法。</span><span class="sxs-lookup"><span data-stu-id="fb48e-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="fb48e-119">請注意，傳遞物件的 [**Id**](-wia-iwiadeviceinfo-id.md) 屬性會導致完全相同的行為。</span><span class="sxs-lookup"><span data-stu-id="fb48e-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



<span data-ttu-id="fb48e-120">在下一個範例中，呼叫應用程式會將集合中 [**DeviceInfo**](-wia-deviceinfo.md) 物件的索引傳遞給 **Create** 方法。</span><span class="sxs-lookup"><span data-stu-id="fb48e-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



<span data-ttu-id="fb48e-121">下一個範例會傳遞 **Nothing** 給 **Create** 方法，以顯示可讓使用者選取裝置的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fb48e-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="fb48e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb48e-122">Requirements</span></span>



| <span data-ttu-id="fb48e-123">需求</span><span class="sxs-lookup"><span data-stu-id="fb48e-123">Requirement</span></span> | <span data-ttu-id="fb48e-124">值</span><span class="sxs-lookup"><span data-stu-id="fb48e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb48e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb48e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fb48e-126">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb48e-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb48e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb48e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fb48e-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb48e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fb48e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fb48e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb48e-130"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="fb48e-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




