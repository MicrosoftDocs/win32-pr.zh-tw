---
description: Windows 感應器和位置平台會定義驅動程式事件的常數。 感應器 manfuactureres 也可以定義自己的常數。
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: " (感應器的事件常數。 h) "
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996859"
---
# <a name="event-constants-sensorsh"></a><span data-ttu-id="04123-104"> (感應器的事件常數。 h) </span><span class="sxs-lookup"><span data-stu-id="04123-104">Event Constants (Sensors.h)</span></span>

<span data-ttu-id="04123-105">Windows 感應器和位置平台會定義驅動程式事件的常數。</span><span class="sxs-lookup"><span data-stu-id="04123-105">The Windows Sensor and Location platform defines constants for driver events.</span></span> <span data-ttu-id="04123-106">感應器 manfuactureres 也可以定義自己的常數。</span><span class="sxs-lookup"><span data-stu-id="04123-106">Sensor manfuactureres can also define their own constants.</span></span>

<span data-ttu-id="04123-107">**感應器事件種類**</span><span class="sxs-lookup"><span data-stu-id="04123-107">**Sensor Event Types**</span></span>

<span data-ttu-id="04123-108">平臺會定義下列感應器事件種類識別碼。</span><span class="sxs-lookup"><span data-stu-id="04123-108">The platform defines the following sensor event type identifiers.</span></span>



| <span data-ttu-id="04123-109">感應器事件種類</span><span class="sxs-lookup"><span data-stu-id="04123-109">Sensor event type</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="04123-110">Description</span><span class="sxs-lookup"><span data-stu-id="04123-110">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <span data-ttu-id="04123-111"><dt>**感應器 \_事件 \_ 加速計 \_ 搖動**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span><span class="sxs-lookup"><span data-stu-id="04123-111"><dt>**SENSOR\_EVENT\_ACCELEROMETER\_SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span></span> </dl> | <span data-ttu-id="04123-112">指出裝置已 shaken。</span><span class="sxs-lookup"><span data-stu-id="04123-112">Indicates that the device was shaken.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <span data-ttu-id="04123-113"><dt>**感應器 \_\_ \_ 已更新事件資料**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span><span class="sxs-lookup"><span data-stu-id="04123-113"><dt>**SENSOR\_EVENT\_DATA\_UPDATED**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span></span> </dl>                      | <span data-ttu-id="04123-114">指出有新的資料可供使用。</span><span class="sxs-lookup"><span data-stu-id="04123-114">Indicates that new data is available.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <span data-ttu-id="04123-115"><dt>**感應器 \_事件 \_ 屬性 \_ 已變更**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span><span class="sxs-lookup"><span data-stu-id="04123-115"><dt>**SENSOR\_EVENT\_PROPERTY\_CHANGED**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span></span> </dl>          | <span data-ttu-id="04123-116">表示屬性值已變更。</span><span class="sxs-lookup"><span data-stu-id="04123-116">Indicates that a property value changed.</span></span> <span data-ttu-id="04123-117">檢查 [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) 介面（透過 *pEventData* 參數傳遞至 [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent)），以判斷已變更的屬性及其新值。</span><span class="sxs-lookup"><span data-stu-id="04123-117">Check the [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface, passed through the *pEventData* parameter to [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), to determine which property changed and its new value.</span></span><br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <span data-ttu-id="04123-118"><dt>**感應器 \_事件 \_ 狀態 \_ 已變更**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span><span class="sxs-lookup"><span data-stu-id="04123-118"><dt>**SENSOR\_EVENT\_STATE\_CHANGED**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span></span> </dl>                   | <span data-ttu-id="04123-119">表示作業狀態的變更，例如，從感應器 \_ 狀態 \_ 初始化至感應器 \_ 狀態 \_ 就緒。</span><span class="sxs-lookup"><span data-stu-id="04123-119">Indicates a change of operational state, for example, from SENSOR\_STATE\_INITIALIZING to SENSOR\_STATE\_READY.</span></span><br/>                                                                                                                                                                                            |



<span data-ttu-id="04123-120">**感應器事件 PROPERTYKEYs**</span><span class="sxs-lookup"><span data-stu-id="04123-120">**Sensor Event PROPERTYKEYs**</span></span>

<span data-ttu-id="04123-121">事件的平臺定義屬性索引鍵是以下列 GUID 為基礎：</span><span class="sxs-lookup"><span data-stu-id="04123-121">Platform-defined property keys for events are based on the following GUID:</span></span>

<span data-ttu-id="04123-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span><span class="sxs-lookup"><span data-stu-id="04123-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span></span>

<span data-ttu-id="04123-123">感應器平臺會定義下列可識別感應器事件參數的 **PROPERTYKEY**。</span><span class="sxs-lookup"><span data-stu-id="04123-123">The sensor platform defines the following **PROPERTYKEY** s that identify sensor event parameters.</span></span>



| <span data-ttu-id="04123-124">感應器事件 PROPERTYKEY 和 PID</span><span class="sxs-lookup"><span data-stu-id="04123-124">Sensor event PROPERTYKEY and PID</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="04123-125">Description</span><span class="sxs-lookup"><span data-stu-id="04123-125">Description</span></span>                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <span data-ttu-id="04123-126"><dt>**感應器 \_事件 \_ 參數 \_ 事件 \_ 識別碼**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="04123-126"><dt>**SENSOR\_EVENT\_PARAMETER\_EVENT\_ID**</dt> <dt>(PID = 2)</dt></span></span> </dl> | <span data-ttu-id="04123-127">指出 [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))中的 **GUID** 值是事件種類識別碼，例如更新的感應器 \_ 事件 \_ 資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="04123-127">Indicates that the **GUID** value in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) is an event type ID, such as SENSOR\_EVENT\_DATA\_UPDATED.</span></span><br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <span data-ttu-id="04123-128"><dt>**感應器 \_事件 \_ 參數 \_ 狀態**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="04123-128"><dt>**SENSOR\_EVENT\_PARAMETER\_STATE**</dt> <dt>(PID = 3)</dt></span></span> </dl>           | <span data-ttu-id="04123-129">指出 **IPortableDeviceValues** 中不帶正負號的整數值為感應器狀態，例如感應器 \_ 狀態 \_ 就緒。</span><span class="sxs-lookup"><span data-stu-id="04123-129">Indicates that the unsigned integer value in **IPortableDeviceValues** is a sensor state, such as SENSOR\_STATE\_READY.</span></span><br/>                                                  |



<span data-ttu-id="04123-130">**感應器錯誤 PROPERTYKEYs**</span><span class="sxs-lookup"><span data-stu-id="04123-130">**Sensor Error PROPERTYKEYs**</span></span>

<span data-ttu-id="04123-131">適用于錯誤的平臺定義屬性索引鍵會以下列 GUID 為基礎：</span><span class="sxs-lookup"><span data-stu-id="04123-131">Platform-defined property keys for errors will be based on the following GUID:</span></span>

<span data-ttu-id="04123-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span><span class="sxs-lookup"><span data-stu-id="04123-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span></span>

<span data-ttu-id="04123-133">感應器平臺會保留此 GUID 供日後使用。</span><span class="sxs-lookup"><span data-stu-id="04123-133">The sensor platform reserves this GUID for future use.</span></span>

<dl></dl>

## <a name="requirements"></a><span data-ttu-id="04123-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="04123-134">Requirements</span></span>



| <span data-ttu-id="04123-135">需求</span><span class="sxs-lookup"><span data-stu-id="04123-135">Requirement</span></span> | <span data-ttu-id="04123-136">值</span><span class="sxs-lookup"><span data-stu-id="04123-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04123-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04123-137">Minimum supported client</span></span><br/> | <span data-ttu-id="04123-138">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04123-138">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="04123-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04123-139">Minimum supported server</span></span><br/> | <span data-ttu-id="04123-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="04123-140">None supported</span></span><br/>                                                            |
| <span data-ttu-id="04123-141">標頭</span><span class="sxs-lookup"><span data-stu-id="04123-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="04123-142"><dt>感應器。h</dt></span><span class="sxs-lookup"><span data-stu-id="04123-142"><dt>Sensors.h</dt></span></span> </dl> |



 

