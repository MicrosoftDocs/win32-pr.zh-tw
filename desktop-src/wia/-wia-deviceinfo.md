---
description: DeviceInfo 物件可讓您存取 Windows 映像取得 (WIA) 硬體裝置的屬性。
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: DeviceInfo 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979788"
---
# <a name="deviceinfo-object"></a><span data-ttu-id="3c5ac-103">DeviceInfo 物件</span><span class="sxs-lookup"><span data-stu-id="3c5ac-103">DeviceInfo object</span></span>

<span data-ttu-id="3c5ac-104">**DeviceInfo** 物件可讓您存取 Windows 映像取得 (WIA) 硬體裝置的屬性。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-104">The **DeviceInfo** object provides access to the properties of a Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="3c5ac-105">它也會透過其 [**建立**](-wia-iwiadeviceinfo-create.md) 方法，提供一個方法讓應用程式或腳本連線到裝置，並取得代表裝置的 [**專案**](-wia-item.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-105">It also, through its [**Create**](-wia-iwiadeviceinfo-create.md) method, provides a way for the application or script to connect to the device and obtain an [**Item**](-wia-item.md) object that represents the device.</span></span> <span data-ttu-id="3c5ac-106">使用 [**Devices**](-wia-iwia-devices.md) 方法取得 **DeviceInfo** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-106">Use the [**Devices**](-wia-iwia-devices.md) method to obtain a collection of **DeviceInfo** objects.</span></span>

## <a name="members"></a><span data-ttu-id="3c5ac-107">成員</span><span class="sxs-lookup"><span data-stu-id="3c5ac-107">Members</span></span>

<span data-ttu-id="3c5ac-108">**DeviceInfo** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3c5ac-108">The **DeviceInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="3c5ac-109">方法</span><span class="sxs-lookup"><span data-stu-id="3c5ac-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c5ac-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3c5ac-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3c5ac-111">方法</span><span class="sxs-lookup"><span data-stu-id="3c5ac-111">Methods</span></span>

<span data-ttu-id="3c5ac-112">**DeviceInfo** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-112">The **DeviceInfo** object has these methods.</span></span>



| <span data-ttu-id="3c5ac-113">方法</span><span class="sxs-lookup"><span data-stu-id="3c5ac-113">Method</span></span>                                                 | <span data-ttu-id="3c5ac-114">描述</span><span class="sxs-lookup"><span data-stu-id="3c5ac-114">Description</span></span>                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c5ac-115">**創建**</span><span class="sxs-lookup"><span data-stu-id="3c5ac-115">**Create**</span></span>](-wia-iwiadeviceinfo-create.md)           | <span data-ttu-id="3c5ac-116">**DeviceInfo** 物件的 [**Create**](-wia-iwiadeviceinfo-create.md)方法會連接到 **DEVICEINFO** 物件所指定的 WIA 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-116">The [**Create**](-wia-iwiadeviceinfo-create.md) method of the **DeviceInfo** object makes a connection to the WIA device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |
| [<span data-ttu-id="3c5ac-117">**GetPropById**</span><span class="sxs-lookup"><span data-stu-id="3c5ac-117">**GetPropById**</span></span>](-wia-iwiadeviceinfo-getpropbyid.md) | <span data-ttu-id="3c5ac-118">**DeviceInfo** 物件的 [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md)方法會使用裝置屬性的識別碼來傳回其值。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-118">The [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) method of the **DeviceInfo** object uses a device property's ID to return its value.</span></span><br/>                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="3c5ac-119">屬性</span><span class="sxs-lookup"><span data-stu-id="3c5ac-119">Properties</span></span>

<span data-ttu-id="3c5ac-120">**DeviceInfo** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-120">The **DeviceInfo** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3c5ac-121">屬性</span><span class="sxs-lookup"><span data-stu-id="3c5ac-121">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3c5ac-122">存取類型</span><span class="sxs-lookup"><span data-stu-id="3c5ac-122">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3c5ac-123">Description</span><span class="sxs-lookup"><span data-stu-id="3c5ac-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3c5ac-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c5ac-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c5ac-125">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-126">捕獲 WIA 硬體裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-126">Retrieves the ID of the WIA hardware device.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3c5ac-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>製造商</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c5ac-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c5ac-128">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-129">抓取此硬體裝置的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-129">Retrieves the name of the manufacturer of this hardware device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3c5ac-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c5ac-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c5ac-131">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-132">顯示在 UI 中的 WIA 硬體裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-132">The name of the WIA hardware device as it appears in the UI.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3c5ac-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>連接埠</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c5ac-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c5ac-134">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-135">捕獲 WIA 硬體裝置所連接的埠。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-135">Retrieves the port to which the WIA hardware device is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3c5ac-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>類型</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c5ac-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c5ac-137">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-138">捕獲 WIA 硬體裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-138">Retrieves the type of WIA hardware device.</span></span> <span data-ttu-id="3c5ac-139">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="3c5ac-139">Possible values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="3c5ac-140">DigitalCamera</span><span class="sxs-lookup"><span data-stu-id="3c5ac-140">DigitalCamera</span></span></li>
<li><span data-ttu-id="3c5ac-141">掃描器</span><span class="sxs-lookup"><span data-stu-id="3c5ac-141">Scanner</span></span></li>
<li><span data-ttu-id="3c5ac-142">StreamingVideo</span><span class="sxs-lookup"><span data-stu-id="3c5ac-142">StreamingVideo</span></span></li>
<li><span data-ttu-id="3c5ac-143">預設</span><span class="sxs-lookup"><span data-stu-id="3c5ac-143">Default</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3c5ac-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span><span class="sxs-lookup"><span data-stu-id="3c5ac-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-145">唯讀</span><span class="sxs-lookup"><span data-stu-id="3c5ac-145">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="3c5ac-146">抓取此 WIA 硬體裝置製造商提供之使用者介面的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-146">Retrieves the class id of the manufacturer-provided user interface for this WIA hardware device.</span></span> <span data-ttu-id="3c5ac-147">值是 GUID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="3c5ac-147">The value is a string representation of a GUID.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3c5ac-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c5ac-148">Requirements</span></span>



| <span data-ttu-id="3c5ac-149">需求</span><span class="sxs-lookup"><span data-stu-id="3c5ac-149">Requirement</span></span> | <span data-ttu-id="3c5ac-150">值</span><span class="sxs-lookup"><span data-stu-id="3c5ac-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5ac-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c5ac-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5ac-152">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c5ac-152">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c5ac-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c5ac-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5ac-154">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c5ac-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3c5ac-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3c5ac-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c5ac-156"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3c5ac-156"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




