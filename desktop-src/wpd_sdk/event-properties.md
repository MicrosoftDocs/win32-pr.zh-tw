---
description: Windows 可攜式裝置支援下列事件屬性。
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: '事件屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998684"
---
# <a name="event-properties"></a><span data-ttu-id="26091-103">事件屬性</span><span class="sxs-lookup"><span data-stu-id="26091-103">Event Properties</span></span>

<span data-ttu-id="26091-104">Windows 可攜式裝置支援下列事件屬性。</span><span class="sxs-lookup"><span data-stu-id="26091-104">Windows Portable Devices supports the following event properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26091-105">屬性</span><span class="sxs-lookup"><span data-stu-id="26091-105">Property</span></span></th>
<th><span data-ttu-id="26091-106">VarType</span><span class="sxs-lookup"><span data-stu-id="26091-106">VarType</span></span></th>
<th><span data-ttu-id="26091-107">Description</span><span class="sxs-lookup"><span data-stu-id="26091-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26091-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="26091-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span></span></td>
<td><span data-ttu-id="26091-109"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="26091-109"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="26091-110">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="26091-110">Reserved for future use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26091-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="26091-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span></span></td>
<td><span data-ttu-id="26091-112"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="26091-112"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="26091-113">布林值，指定是否要將事件廣播至所有用戶端。用戶端可以藉由向 <strong>IPortableDevice：： Advise</strong>註冊回呼，來接收此事件。</span><span class="sxs-lookup"><span data-stu-id="26091-113">A Boolean value that specifies whether the event is broadcast to all clients.Clients can receive this event by registering their callback with <strong>IPortableDevice::Advise</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26091-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span><span class="sxs-lookup"><span data-stu-id="26091-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span></span></td>
<td><span data-ttu-id="26091-115"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="26091-115"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="26091-116">布林值，指定物件的子階層是否已變更。這個參數是用來通知呼叫端，已新增或移除指定之物件的某些子系。</span><span class="sxs-lookup"><span data-stu-id="26091-116">A Boolean value that specifies whether the child hierarchy for the object has changed.This parameter is used to notify the caller that some children for the specified object have been added or removed.</span></span> <span data-ttu-id="26091-117">通常會在裝置端起始階層變更。</span><span class="sxs-lookup"><span data-stu-id="26091-117">Typically the hierarchy change is initiated on the device side.</span></span> <span data-ttu-id="26091-118">用戶端可能必須重新列舉這個資料夾的子系，才能讓他們的觀點保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="26091-118">Clients may have to re-enumerate this folder's children to keep their views up to date.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26091-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span><span class="sxs-lookup"><span data-stu-id="26091-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span></span></td>
<td><span data-ttu-id="26091-120"><strong>VT_CLSID</strong></span><span class="sxs-lookup"><span data-stu-id="26091-120"><strong>VT_CLSID</strong></span></span></td>
<td><span data-ttu-id="26091-121">識別事件的值。</span><span class="sxs-lookup"><span data-stu-id="26091-121">A value that identifies an event.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26091-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span><span class="sxs-lookup"><span data-stu-id="26091-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span></span></td>
<td><span data-ttu-id="26091-123"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="26091-123"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="26091-124">當 cookie 透過呼叫 <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent：： CreateObjectWithPropertiesAndData</strong></a> 方法要求建立物件時，會將 cookie 回傳給用戶端。加入這個參數是為了方便呼叫者將已加入物件的事件系結至它所傳送的要求，以建立物件。</span><span class="sxs-lookup"><span data-stu-id="26091-124">The cookie handed back to a client when it requests an object creation by calling the <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent::CreateObjectWithPropertiesAndData</strong></a> method.This parameter is added as a convenience to help the caller tie an object-added event to the request it sent to create the object.</span></span> <span data-ttu-id="26091-125">驅動程式會在處理<strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong>命令時，將此 cookie 回傳為<strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong>傳回值。</span><span class="sxs-lookup"><span data-stu-id="26091-125">The driver hands this cookie back as the <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> return value when processing the <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26091-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="26091-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="26091-127"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="26091-127"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="26091-128">可唯一識別父物件的值。</span><span class="sxs-lookup"><span data-stu-id="26091-128">A value that uniquely identifies the parent object.</span></span> <span data-ttu-id="26091-129">這個屬性類似于 <strong>WPD_OBJECT_PARENT_ID</strong>，但此識別碼不會在會話之間變更。</span><span class="sxs-lookup"><span data-stu-id="26091-129">This property is similar to <strong>WPD_OBJECT_PARENT_ID</strong>, but this ID does not change between sessions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26091-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span><span class="sxs-lookup"><span data-stu-id="26091-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span></span></td>
<td><span data-ttu-id="26091-131"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="26091-131"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="26091-132">值，指定目前執行中作業的進度。</span><span class="sxs-lookup"><span data-stu-id="26091-132">A value that specifies the progress of a currently executing operation.</span></span> <span data-ttu-id="26091-133">這個屬性的值的範圍可以從0到100，而100則表示作業已完成。</span><span class="sxs-lookup"><span data-stu-id="26091-133">The value of this property can range from 0 to 100, with 100 indicating that the operation is complete.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26091-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span><span class="sxs-lookup"><span data-stu-id="26091-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span></span></td>
<td><span data-ttu-id="26091-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="26091-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="26091-136">值，指出作業的目前狀態，例如，已啟動、執行中、已停止等等。這個參數的可能值是來自 PortableDevice 中定義的 <strong>WPD_OPERATION_STATES</strong> 列舉。</span><span class="sxs-lookup"><span data-stu-id="26091-136">A value that indicates the current state of the operation, for example, started, running, stopped, and so on.This parameter's possible values are from the <strong>WPD_OPERATION_STATES</strong> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="26091-137">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="26091-137">Possible values are:</span></span><br/> <dl> <span data-ttu-id="26091-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span><span class="sxs-lookup"><span data-stu-id="26091-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span></span><br /><span data-ttu-id="26091-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span><span class="sxs-lookup"><span data-stu-id="26091-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span></span><br /><span data-ttu-id="26091-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="26091-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span></span><br /><span data-ttu-id="26091-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span><span class="sxs-lookup"><span data-stu-id="26091-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span></span><br /><span data-ttu-id="26091-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="26091-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span></span><br /><span data-ttu-id="26091-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span><span class="sxs-lookup"><span data-stu-id="26091-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span></span><br /><span data-ttu-id="26091-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span><span class="sxs-lookup"><span data-stu-id="26091-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26091-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="26091-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span></span></td>
<td><span data-ttu-id="26091-146"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="26091-146"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="26091-147">值，指定產生事件的裝置。這是隨插即用 (PnP) 系統所提供的裝置或服務識別碼，與 <strong>IPortableDevice：： open</strong>或 <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService：： open</strong></a> 方法中使用的字串相同。</span><span class="sxs-lookup"><span data-stu-id="26091-147">A value that specifies the device that originated the event.This is the device or service identifier given by the Plug-and-Play (PnP) system, and is the same string used in the <strong>IPortableDevice::Open</strong>or <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26091-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span><span class="sxs-lookup"><span data-stu-id="26091-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span></span></td>
<td><span data-ttu-id="26091-149"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="26091-149"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="26091-150">WPD 驅動程式用來識別裝置服務方法之作業的字串。</span><span class="sxs-lookup"><span data-stu-id="26091-150">A string that is used by a WPD driver to identify the operation of a device-service method.</span></span> <span data-ttu-id="26091-151">應用程式不應直接使用此參數。</span><span class="sxs-lookup"><span data-stu-id="26091-151">Applications should not use this parameter directly.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="26091-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="26091-152">Requirements</span></span>



| <span data-ttu-id="26091-153">需求</span><span class="sxs-lookup"><span data-stu-id="26091-153">Requirement</span></span> | <span data-ttu-id="26091-154">值</span><span class="sxs-lookup"><span data-stu-id="26091-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="26091-155">標頭</span><span class="sxs-lookup"><span data-stu-id="26091-155">Header</span></span><br/> | <dl> <span data-ttu-id="26091-156"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="26091-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26091-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26091-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26091-158">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="26091-158">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




