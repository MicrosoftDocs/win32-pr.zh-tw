---
description: Wia 物件是所有 Windows 映像取得 (WIA) 腳本功能的進入點。
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Wia 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113264"
---
# <a name="wia-object"></a><span data-ttu-id="4317a-103">Wia 物件</span><span class="sxs-lookup"><span data-stu-id="4317a-103">Wia object</span></span>

<span data-ttu-id="4317a-104">**Wia** 物件是所有 Windows 映像取得 (Wia) 腳本功能的進入點。</span><span class="sxs-lookup"><span data-stu-id="4317a-104">The **Wia** object is the entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="4317a-105">使用 WIA 腳本模型的任何應用程式都必須建立 [**SafeWia**](-wia-safewia.md) 或 **WIA** 物件。</span><span class="sxs-lookup"><span data-stu-id="4317a-105">Any application that uses the WIA scripting model must create a [**SafeWia**](-wia-safewia.md) or **Wia** object.</span></span> <span data-ttu-id="4317a-106">您可以使用該物件來列舉和建立裝置，並接收硬體事件的通知。</span><span class="sxs-lookup"><span data-stu-id="4317a-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

> [!Note]  
> <span data-ttu-id="4317a-107">此物件對腳本而言並不安全。</span><span class="sxs-lookup"><span data-stu-id="4317a-107">This object is not safe for scripting.</span></span> <span data-ttu-id="4317a-108">如需此物件可安全地進行腳本處理的版本，請參閱 [**SafeWia**](-wia-safewia.md)。</span><span class="sxs-lookup"><span data-stu-id="4317a-108">For a version of this object that is safe for scripting, see [**SafeWia**](-wia-safewia.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="4317a-109">成員</span><span class="sxs-lookup"><span data-stu-id="4317a-109">Members</span></span>

<span data-ttu-id="4317a-110">**Wia** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4317a-110">The **Wia** object has these types of members:</span></span>

-   [<span data-ttu-id="4317a-111">事件</span><span class="sxs-lookup"><span data-stu-id="4317a-111">Events</span></span>](#events)
-   [<span data-ttu-id="4317a-112">方法</span><span class="sxs-lookup"><span data-stu-id="4317a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4317a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4317a-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="4317a-114">事件</span><span class="sxs-lookup"><span data-stu-id="4317a-114">Events</span></span>

<span data-ttu-id="4317a-115">**Wia** 物件具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="4317a-115">The **Wia** object has these events.</span></span>



| <span data-ttu-id="4317a-116">事件</span><span class="sxs-lookup"><span data-stu-id="4317a-116">Event</span></span>                                                                 | <span data-ttu-id="4317a-117">描述</span><span class="sxs-lookup"><span data-stu-id="4317a-117">Description</span></span>                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="4317a-118">**OnDeviceConnected**</span><span class="sxs-lookup"><span data-stu-id="4317a-118">**OnDeviceConnected**</span></span>](-wia--iwiaevents-ondeviceconnected.md)       | <span data-ttu-id="4317a-119">連接新的 WIA 硬體裝置時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="4317a-119">Event that occurs when a new WIA hardware device is connected.</span></span><br/>    |
| [<span data-ttu-id="4317a-120">**OnDeviceDisconnected**</span><span class="sxs-lookup"><span data-stu-id="4317a-120">**OnDeviceDisconnected**</span></span>](-wia--iwiaevents-ondevicedisconnected.md) | <span data-ttu-id="4317a-121">當新的 WIA 硬體裝置中斷連線時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="4317a-121">Event that occurs when a new WIA hardware device is disconnected.</span></span><br/> |
| [<span data-ttu-id="4317a-122">**OnTransferComplete**</span><span class="sxs-lookup"><span data-stu-id="4317a-122">**OnTransferComplete**</span></span>](-wia--iwiaevents-ontransfercomplete.md)     | <span data-ttu-id="4317a-123">成功完成資料傳輸時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="4317a-123">Event that occurs when a data transfer is completed successfully.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="4317a-124">方法</span><span class="sxs-lookup"><span data-stu-id="4317a-124">Methods</span></span>

<span data-ttu-id="4317a-125">**Wia** 物件具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4317a-125">The **Wia** object has these methods.</span></span>



| <span data-ttu-id="4317a-126">方法</span><span class="sxs-lookup"><span data-stu-id="4317a-126">Method</span></span>                             | <span data-ttu-id="4317a-127">描述</span><span class="sxs-lookup"><span data-stu-id="4317a-127">Description</span></span>                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4317a-128">**創建**</span><span class="sxs-lookup"><span data-stu-id="4317a-128">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="4317a-129">**Wia** 物件的 [**Create**](-wia-iwia-create.md)方法會連接到指定的 Wia 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。</span><span class="sxs-lookup"><span data-stu-id="4317a-129">The [**Create**](-wia-iwia-create.md) method of the **Wia** object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4317a-130">屬性</span><span class="sxs-lookup"><span data-stu-id="4317a-130">Properties</span></span>

<span data-ttu-id="4317a-131">**Wia** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4317a-131">The **Wia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4317a-132">屬性</span><span class="sxs-lookup"><span data-stu-id="4317a-132">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4317a-133">存取類型</span><span class="sxs-lookup"><span data-stu-id="4317a-133">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4317a-134">Description</span><span class="sxs-lookup"><span data-stu-id="4317a-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4317a-135"><a href="-wia-iwia-devices.md"><strong>設備</strong></a></span><span class="sxs-lookup"><span data-stu-id="4317a-135"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="4317a-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="4317a-136">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="4317a-137"><a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a>物件的集合，代表安裝在電腦上的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="4317a-137">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="4317a-138">唯讀。</span><span class="sxs-lookup"><span data-stu-id="4317a-138">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4317a-139">這個集合是以0為基礎。</span><span class="sxs-lookup"><span data-stu-id="4317a-139">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="4317a-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="4317a-140">Requirements</span></span>



| <span data-ttu-id="4317a-141">需求</span><span class="sxs-lookup"><span data-stu-id="4317a-141">Requirement</span></span> | <span data-ttu-id="4317a-142">值</span><span class="sxs-lookup"><span data-stu-id="4317a-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4317a-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4317a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4317a-144">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4317a-144">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4317a-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4317a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4317a-146">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4317a-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4317a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4317a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4317a-148"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="4317a-148"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="4317a-149">IID</span><span class="sxs-lookup"><span data-stu-id="4317a-149">IID</span></span><br/>                      | <span data-ttu-id="4317a-150">CLSID \_ Wia</span><span class="sxs-lookup"><span data-stu-id="4317a-150">CLSID\_Wia</span></span><br/>                                                                                         |



 

 




