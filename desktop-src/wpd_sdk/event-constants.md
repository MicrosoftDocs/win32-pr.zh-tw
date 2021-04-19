---
description: Windows 可攜式裝置會定義下列事件值。
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: " (PortableDevice 的事件常數) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992945"
---
# <a name="event-constants-portabledeviceh"></a><span data-ttu-id="08ff7-103"> (PortableDevice 的事件常數) </span><span class="sxs-lookup"><span data-stu-id="08ff7-103">Event Constants (PortableDevice.h)</span></span>

<span data-ttu-id="08ff7-104">Windows 可攜式裝置會定義下列事件值。</span><span class="sxs-lookup"><span data-stu-id="08ff7-104">Windows Portable Devices defines the following event values.</span></span>



| <span data-ttu-id="08ff7-105">常數</span><span class="sxs-lookup"><span data-stu-id="08ff7-105">Constant</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="08ff7-106">描述</span><span class="sxs-lookup"><span data-stu-id="08ff7-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <span data-ttu-id="08ff7-107"><dt>**\_已更新 WPD 事件 \_ 裝置 \_ 功能 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-107"><dt>**WPD\_EVENT\_DEVICE\_CAPABILITIES\_UPDATED**</dt></span></span> </dl> | <span data-ttu-id="08ff7-108">此事件表示裝置功能已變更。</span><span class="sxs-lookup"><span data-stu-id="08ff7-108">This event indicates that the device capabilities have changed.</span></span> <span data-ttu-id="08ff7-109">如果用戶端根據裝置功能做出任何決策，則應該重新查詢裝置。</span><span class="sxs-lookup"><span data-stu-id="08ff7-109">Clients should requery the device if they have made any decisions based on device capabilities.</span></span><br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <span data-ttu-id="08ff7-110"><dt>**\_ \_ 已移除 WPD 事件裝置 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-110"><dt>**WPD\_EVENT\_DEVICE\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="08ff7-111">當卸載裝置的驅動程式時，就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="08ff7-111">This event is sent when a driver for a device is being unloaded.</span></span> <span data-ttu-id="08ff7-112">這通常是裝置即將插即用的結果。</span><span class="sxs-lookup"><span data-stu-id="08ff7-112">Typically this is a result of the device being unplugged.</span></span><br/> <span data-ttu-id="08ff7-113">用戶端應該釋放 **IPortableDevice** 介面，以及在 **WPD \_ 事件 \_ 參數 \_ PNP \_ 裝置 \_ 識別碼** 中指定的任何 [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)介面。</span><span class="sxs-lookup"><span data-stu-id="08ff7-113">Clients should release the **IPortableDevice** interface and any [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) interfaces specified in **WPD\_EVENT\_PARAMETER\_PNP\_DEVICE\_ID**.</span></span><br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <span data-ttu-id="08ff7-114"><dt>**WPD \_ 事件 \_ 裝置 \_ 重設**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-114"><dt>**WPD\_EVENT\_DEVICE\_RESET**</dt></span></span> </dl>                                               | <span data-ttu-id="08ff7-115">此事件表示裝置即將重設，而且所有連線的用戶端都應該關閉其與裝置的連線。</span><span class="sxs-lookup"><span data-stu-id="08ff7-115">This event indicates that the device is about to be reset, and all connected clients should close their connections to the device.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <span data-ttu-id="08ff7-116"><dt>**\_ \_ 已新增 WPD 事件物件 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-116"><dt>**WPD\_EVENT\_OBJECT\_ADDED**</dt></span></span> </dl>                                               | <span data-ttu-id="08ff7-117">此事件表示裝置上有新的物件可用。</span><span class="sxs-lookup"><span data-stu-id="08ff7-117">This event indicates that a new object is available on the device.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <span data-ttu-id="08ff7-118"><dt>**WPD \_ 事件 \_ 物件 \_ 已移除**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-118"><dt>**WPD\_EVENT\_OBJECT\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="08ff7-119">從裝置移除先前現有的物件之後，就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="08ff7-119">This event is sent after a previously existing object has been removed from the device.</span></span><br/> <span data-ttu-id="08ff7-120">物件可能是內容物件，例如，已刪除影像檔案。或者，它可能是一個功能物件，例如，新的儲存裝置已從裝置中拔出。</span><span class="sxs-lookup"><span data-stu-id="08ff7-120">The object might be a content object, for example, an image file was deleted; or it might be a functional object, for example, a new storage device was unplugged from the device.</span></span><br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <span data-ttu-id="08ff7-121"><dt>**已 \_ 要求 WPD 事件 \_ 物件 \_ 傳輸 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-121"><dt>**WPD\_EVENT\_OBJECT\_TRANSFER\_REQUESTED**</dt></span></span> </dl>       | <span data-ttu-id="08ff7-122">系統會傳送此事件以要求應用程式從裝置傳送特定物件。</span><span class="sxs-lookup"><span data-stu-id="08ff7-122">This event is sent to request an application to transfer a particular object from the device.</span></span><br/> <span data-ttu-id="08ff7-123">物件通常是內容物件，例如影像檔案。</span><span class="sxs-lookup"><span data-stu-id="08ff7-123">The object is usually a content object, for example, an image file.</span></span><br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <span data-ttu-id="08ff7-124"><dt>**WPD \_ 事件 \_ 物件 \_ 已更新**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-124"><dt>**WPD\_EVENT\_OBJECT\_UPDATED**</dt></span></span> </dl>                                         | <span data-ttu-id="08ff7-125">此事件是在物件已更新之後傳送，而且任何連線的用戶端都應該重新整理該物件的觀點。</span><span class="sxs-lookup"><span data-stu-id="08ff7-125">This event is sent after an object has been updated, and any connected client should refresh its view of that object.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <span data-ttu-id="08ff7-126"><dt>**WPD \_ 事件 \_ 服務 \_ 方法 \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-126"><dt>**WPD\_EVENT\_SERVICE\_METHOD\_COMPLETE**</dt></span></span> </dl>             | <span data-ttu-id="08ff7-127">當驅動程式已完成叫用服務方法時，就會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="08ff7-127">This event is sent when a driver has completed invoking a service method.</span></span> <span data-ttu-id="08ff7-128">即使方法失敗，也必須傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="08ff7-128">This event must be sent even when the method fails.</span></span> <span data-ttu-id="08ff7-129">這是內部 WPD 的 DDI 事件，任何應用程式都不會透過 [**IPortableDevice：： Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) 或 [**IPortableDeviceService：： advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise)提供使用。</span><span class="sxs-lookup"><span data-stu-id="08ff7-129">This is an internal WPD DDI event, and will not be available to any applications through [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) or [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span></span><br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <span data-ttu-id="08ff7-130"><dt>**WPD \_ 事件 \_ 儲存 \_ 格式**</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-130"><dt>**WPD\_EVENT\_STORAGE\_FORMAT**</dt></span></span> </dl>                                         | <span data-ttu-id="08ff7-131">此事件表示儲存物件上的格式作業進度。</span><span class="sxs-lookup"><span data-stu-id="08ff7-131">This event indicates the progress of a format operation on a storage object.</span></span><br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="08ff7-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="08ff7-132">Requirements</span></span>



| <span data-ttu-id="08ff7-133">需求</span><span class="sxs-lookup"><span data-stu-id="08ff7-133">Requirement</span></span> | <span data-ttu-id="08ff7-134">值</span><span class="sxs-lookup"><span data-stu-id="08ff7-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="08ff7-135">標頭</span><span class="sxs-lookup"><span data-stu-id="08ff7-135">Header</span></span><br/> | <dl> <span data-ttu-id="08ff7-136"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="08ff7-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08ff7-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08ff7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ff7-138">常數</span><span class="sxs-lookup"><span data-stu-id="08ff7-138">Constants</span></span>](constants.md)
</dt> </dl>

 

 




