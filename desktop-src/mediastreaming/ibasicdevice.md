---
title: IBasicDevice 介面
description: 封裝為 DLNA 裝置建立模型所需的方法和事件。
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- IBasicDevice 介面媒體串流 API
- IBasicDevice 介面媒體串流 API，說明
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383245"
---
# <a name="ibasicdevice-interface"></a><span data-ttu-id="12924-105">IBasicDevice 介面</span><span class="sxs-lookup"><span data-stu-id="12924-105">IBasicDevice interface</span></span>

<span data-ttu-id="12924-106">封裝為 DLNA 裝置建立模型所需的方法和事件。</span><span class="sxs-lookup"><span data-stu-id="12924-106">Encapsulates the methods and events needed to model a DLNA Device.</span></span>

## <a name="members"></a><span data-ttu-id="12924-107">成員</span><span class="sxs-lookup"><span data-stu-id="12924-107">Members</span></span>

<span data-ttu-id="12924-108">**IBasicDevice** 介面繼承自 [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)。</span><span class="sxs-lookup"><span data-stu-id="12924-108">The **IBasicDevice** interface inherits from [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="12924-109">**IBasicDevice** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="12924-109">**IBasicDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="12924-110">方法</span><span class="sxs-lookup"><span data-stu-id="12924-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="12924-111">方法</span><span class="sxs-lookup"><span data-stu-id="12924-111">Methods</span></span>

<span data-ttu-id="12924-112">**IBasicDevice** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="12924-112">The **IBasicDevice** interface has these methods.</span></span>



| <span data-ttu-id="12924-113">方法</span><span class="sxs-lookup"><span data-stu-id="12924-113">Method</span></span>                                                                                 | <span data-ttu-id="12924-114">描述</span><span class="sxs-lookup"><span data-stu-id="12924-114">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12924-115">**新增 \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="12924-115">**add\_ConnectionStatusChanged**</span></span>](ibasicdevice-add-connectionstatuschanged.md)       | <span data-ttu-id="12924-116">註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="12924-116">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>                |
| [<span data-ttu-id="12924-117">**CanWakeDevices**</span><span class="sxs-lookup"><span data-stu-id="12924-117">**CanWakeDevices**</span></span>](ibasicdevice-canwakedevices.md)                                  | <span data-ttu-id="12924-118">抓取值，指出裝置是否可以喚醒。</span><span class="sxs-lookup"><span data-stu-id="12924-118">Retrieves a value that indicates if the device can wake.</span></span><br/>                                                            |
| <span data-ttu-id="12924-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12924-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span></span>                              | <span data-ttu-id="12924-120">傳回列舉值，指出裝置目前為線上、離線或睡眠中，但可喚醒。</span><span class="sxs-lookup"><span data-stu-id="12924-120">Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.</span></span><br/> |
| [<span data-ttu-id="12924-121">**描述**</span><span class="sxs-lookup"><span data-stu-id="12924-121">**Description**</span></span>](ibasicdevice-description.md)                                        | <span data-ttu-id="12924-122">抓取裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="12924-122">Retrieves a description of the device.</span></span><br/>                                                                              |
| [<span data-ttu-id="12924-123">**DiscoveredOnCurrentNetwork**</span><span class="sxs-lookup"><span data-stu-id="12924-123">**DiscoveredOnCurrentNetwork**</span></span>](ibasicdevice-discoveredoncurrentnetwork.md)          | <span data-ttu-id="12924-124">抓取值，指出裝置是否在目前的網路上。</span><span class="sxs-lookup"><span data-stu-id="12924-124">Retrieves a value that indicates if the device is on the current network.</span></span><br/>                                           |
| [<span data-ttu-id="12924-125">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="12924-125">**FriendlyName**</span></span>](ibasicdevice-friendlyname.md)                                      | <span data-ttu-id="12924-126">抓取裝置的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="12924-126">Retrieves the device s friendly name.</span></span><br/>                                                                               |
| [<span data-ttu-id="12924-127">**圖示**</span><span class="sxs-lookup"><span data-stu-id="12924-127">**Icons**</span></span>](ibasicdevice-icons.md)                                                    | <span data-ttu-id="12924-128">傳回 [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) 介面的向量。</span><span class="sxs-lookup"><span data-stu-id="12924-128">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span><br/>                                                  |
| [<span data-ttu-id="12924-129">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="12924-129">**IpAddresses**</span></span>](ibasicdevice-ipaddresses.md)                                        | <span data-ttu-id="12924-130">傳回 IP 位址的向量。</span><span class="sxs-lookup"><span data-stu-id="12924-130">Returns a vector of IP addresses.</span></span><br/>                                                                                   |
| [<span data-ttu-id="12924-131">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="12924-131">**ManufacturerName**</span></span>](ibasicdevice-manufacturername.md)                              | <span data-ttu-id="12924-132">抓取裝置的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="12924-132">Retrieves the device s manufacturer name.</span></span><br/>                                                                           |
| [<span data-ttu-id="12924-133">**ManufacturerUrl**</span><span class="sxs-lookup"><span data-stu-id="12924-133">**ManufacturerUrl**</span></span>](ibasicdevice-manufacturerurl.md)                                | <span data-ttu-id="12924-134">抓取裝置的製造商 URL。</span><span class="sxs-lookup"><span data-stu-id="12924-134">Retrieves the device s manufacturer URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="12924-135">**ModelName**</span><span class="sxs-lookup"><span data-stu-id="12924-135">**ModelName**</span></span>](ibasicdevice-modelname.md)                                            | <span data-ttu-id="12924-136">抓取裝置的模型名稱。</span><span class="sxs-lookup"><span data-stu-id="12924-136">Retrieves the device s model name.</span></span><br/>                                                                                  |
| [<span data-ttu-id="12924-137">**ModelNumber**</span><span class="sxs-lookup"><span data-stu-id="12924-137">**ModelNumber**</span></span>](ibasicdevice-modelnumber.md)                                        | <span data-ttu-id="12924-138">抓取裝置的模型編號。</span><span class="sxs-lookup"><span data-stu-id="12924-138">Retrieves the device s model number.</span></span><br/>                                                                                |
| [<span data-ttu-id="12924-139">**ModelUrl**</span><span class="sxs-lookup"><span data-stu-id="12924-139">**ModelUrl**</span></span>](ibasicdevice-modelurl.md)                                              | <span data-ttu-id="12924-140">抓取裝置的模型 URL。</span><span class="sxs-lookup"><span data-stu-id="12924-140">Retrieves the device s model URL.</span></span><br/>                                                                                   |
| [<span data-ttu-id="12924-141">**PhysicalAddresses**</span><span class="sxs-lookup"><span data-stu-id="12924-141">**PhysicalAddresses**</span></span>](ibasicdevice-physicaladdresses.md)                            | <span data-ttu-id="12924-142">傳回實體位址的向量。</span><span class="sxs-lookup"><span data-stu-id="12924-142">Returns a vector of physical addresses.</span></span><br/>                                                                             |
| [<span data-ttu-id="12924-143">**PresentationUrl**</span><span class="sxs-lookup"><span data-stu-id="12924-143">**PresentationUrl**</span></span>](ibasicdevice-presentationurl.md)                                | <span data-ttu-id="12924-144">抓取裝置的簡報 URL。</span><span class="sxs-lookup"><span data-stu-id="12924-144">Retrieves the device s presentation URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="12924-145">**RemoteStreamingUrls**</span><span class="sxs-lookup"><span data-stu-id="12924-145">**RemoteStreamingUrls**</span></span>](ibasicdevice-remotestreamingurls.md)                        | <span data-ttu-id="12924-146">傳回遠端串流 Url 的向量。</span><span class="sxs-lookup"><span data-stu-id="12924-146">Returns a vector of remote streaming URLs.</span></span><br/>                                                                          |
| [<span data-ttu-id="12924-147">**移除 \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="12924-147">**remove\_ConnectionStatusChanged**</span></span>](ibasicdevice-remove-connectionstatuschanged.md) | <span data-ttu-id="12924-148">取消註冊 [**ConnectionStatusChanged**](connectionstatuschanged.md) 事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="12924-148">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>              |
| [<span data-ttu-id="12924-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="12924-149">**SerialNumber**</span></span>](ibasicdevice-serialnumber.md)                                      | <span data-ttu-id="12924-150">抓取裝置序號。</span><span class="sxs-lookup"><span data-stu-id="12924-150">Retrieves the device s serial number.</span></span><br/>                                                                               |
| [<span data-ttu-id="12924-151">**類型**</span><span class="sxs-lookup"><span data-stu-id="12924-151">**Type**</span></span>](ibasicdevice-type.md)                                                      | <span data-ttu-id="12924-152">抓取列舉值，指出 DLNA 裝置的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="12924-152">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span><br/>                                       |
| [<span data-ttu-id="12924-153">**UniqueDeviceName**</span><span class="sxs-lookup"><span data-stu-id="12924-153">**UniqueDeviceName**</span></span>](ibasicdevice-uniquedevicename.md)                              | <span data-ttu-id="12924-154">抓取裝置的唯一裝置名稱 (UDN) 。</span><span class="sxs-lookup"><span data-stu-id="12924-154">Retrieves the device s unique device name (UDN).</span></span><br/>                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="12924-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12924-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12924-156">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="12924-156">**IInspectable**</span></span>](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

