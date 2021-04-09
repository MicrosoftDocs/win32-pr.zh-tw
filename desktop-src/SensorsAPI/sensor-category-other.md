---
description: '[感應器 \_ 類別] 類別 \_ 包含的感應器，可支援 HID 類別驅動程式中的自訂類別。'
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: 'SENSOR_CATEGORY_OTHER (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026154"
---
# <a name="sensor_category_other"></a><span data-ttu-id="6eee8-103">其他的感應器 \_ 類別 \_</span><span class="sxs-lookup"><span data-stu-id="6eee8-103">SENSOR\_CATEGORY\_OTHER</span></span>

<span data-ttu-id="6eee8-104">[感應器 \_ 類別] 類別 \_ 包含的感應器，可支援 HID 類別驅動程式中的自訂類別。</span><span class="sxs-lookup"><span data-stu-id="6eee8-104">The SENSOR\_CATEGORY\_OTHER category contains sensors that support the Custom class in the HID Class driver.</span></span>

<dl> <dt>

<span data-ttu-id="6eee8-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**感應器 \_ 類型 \_ 自訂**</span><span class="sxs-lookup"><span data-stu-id="6eee8-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**SENSOR\_TYPE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eee8-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span><span class="sxs-lookup"><span data-stu-id="6eee8-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span></span>
</dt> <dt>



<span data-ttu-id="6eee8-107">支援 HID 類別驅動程式中自訂類別的自訂感應器。</span><span class="sxs-lookup"><span data-stu-id="6eee8-107">Custom sensor that supports the Custom class in the HID Class driver.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="6eee8-108">**平臺定義的資料欄位**</span><span class="sxs-lookup"><span data-stu-id="6eee8-108">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="6eee8-109">此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ 自訂 \_ GUID 為基礎：</span><span class="sxs-lookup"><span data-stu-id="6eee8-109">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_CUSTOM\_GUID:</span></span>

<span data-ttu-id="6eee8-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span><span class="sxs-lookup"><span data-stu-id="6eee8-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span></span>

<span data-ttu-id="6eee8-111">此類別包括下列的平臺定義資料欄位。</span><span class="sxs-lookup"><span data-stu-id="6eee8-111">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="6eee8-112">資料欄位名稱和 PID</span><span class="sxs-lookup"><span data-stu-id="6eee8-112">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="6eee8-113">Description</span><span class="sxs-lookup"><span data-stu-id="6eee8-113">Description</span></span>                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <span data-ttu-id="6eee8-114"><dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ 使用**</dt>方式 <dt> (PID = 5)</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-114"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_USAGE**</dt> <dt> (PID = 5) </dt></span></span> </dl>                          | <span data-ttu-id="6eee8-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="6eee8-115">**VT\_UI4**</span></span><br/> <span data-ttu-id="6eee8-116">可以用來區別多個自訂感應器的 HID 用途。</span><span class="sxs-lookup"><span data-stu-id="6eee8-116">A HID usage which can be used to distinguish multiple, custom sensors.</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <span data-ttu-id="6eee8-117"><dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ 布林 \_ 陣列**</dt> <dt> (PID = 6)</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-117"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_BOOLEAN\_ARRAY**</dt> <dt> (PID = 6) </dt></span></span> </dl> | <span data-ttu-id="6eee8-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="6eee8-118">**VT\_UI4**</span></span><br/> <span data-ttu-id="6eee8-119">指定自訂感應器的布林值陣列。</span><span class="sxs-lookup"><span data-stu-id="6eee8-119">An array of Boolean values for a given custom sensor.</span></span><br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <span data-ttu-id="6eee8-120"><dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE1**</dt> <dt> (PID = 7)</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-120"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE1**</dt> <dt> (PID = 7) </dt></span></span> </dl>                       | <span data-ttu-id="6eee8-121">**VT \_ UI4 \| \| vt \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6eee8-121">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6eee8-122">指定自訂感應器的六個可用值之一。</span><span class="sxs-lookup"><span data-stu-id="6eee8-122">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <span data-ttu-id="6eee8-123"><dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE2**</dt> <dt> (PID = 8)</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-123"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE2**</dt> <dt> (PID = 8) </dt></span></span> </dl>                       | <span data-ttu-id="6eee8-124">**VT \_ UI4 \| \| vt \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6eee8-124">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6eee8-125">指定自訂感應器的六個可用值之一。</span><span class="sxs-lookup"><span data-stu-id="6eee8-125">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <span data-ttu-id="6eee8-126"><dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE3**</dt> <dt> (PID = 9)</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-126"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE3**</dt> <dt> (PID = 9) </dt></span></span> </dl>                       | <span data-ttu-id="6eee8-127">**VT \_ UI4 \| \| vt \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6eee8-127">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6eee8-128">指定自訂感應器的六個可用值之一。</span><span class="sxs-lookup"><span data-stu-id="6eee8-128">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <span data-ttu-id="6eee8-129"><dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE4**</dt> <dt> (PID = 10)</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-129"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE4**</dt> <dt> (PID = 10) </dt></span></span> </dl>                      | <span data-ttu-id="6eee8-130">**VT \_ UI4 \| \| vt \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6eee8-130">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6eee8-131">指定自訂感應器的六個可用值之一。</span><span class="sxs-lookup"><span data-stu-id="6eee8-131">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <span data-ttu-id="6eee8-132"><dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE5**</dt> <dt> (PID = 11)</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-132"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE5**</dt> <dt> (PID = 11) </dt></span></span> </dl>                      | <span data-ttu-id="6eee8-133">**VT \_ UI4 \| \| vt \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6eee8-133">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6eee8-134">指定自訂感應器的六個可用值之一。</span><span class="sxs-lookup"><span data-stu-id="6eee8-134">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <span data-ttu-id="6eee8-135"><dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE6**</dt> <dt> (PID = 12)</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-135"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE6**</dt> <dt> (PID = 12) </dt></span></span> </dl>                      | <span data-ttu-id="6eee8-136">**VT \_ UI4 \| \| vt \_ R4**</span><span class="sxs-lookup"><span data-stu-id="6eee8-136">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="6eee8-137">指定自訂感應器的六個可用值之一。</span><span class="sxs-lookup"><span data-stu-id="6eee8-137">One of six available values for a given custom sensor.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="6eee8-138">備註</span><span class="sxs-lookup"><span data-stu-id="6eee8-138">Remarks</span></span>

<span data-ttu-id="6eee8-139">在 HID 類別驅動程式中支援泛型類別的感應器，會對應至其中一個其他定義的類別， (生物識別、電氣、環境等) 。</span><span class="sxs-lookup"><span data-stu-id="6eee8-139">A sensor that supports the Generic class in the HID class driver will map to one of the other defined categories (biometric, electrical, environmental, and so on).</span></span>

## <a name="requirements"></a><span data-ttu-id="6eee8-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="6eee8-140">Requirements</span></span>



| <span data-ttu-id="6eee8-141">需求</span><span class="sxs-lookup"><span data-stu-id="6eee8-141">Requirement</span></span> | <span data-ttu-id="6eee8-142">值</span><span class="sxs-lookup"><span data-stu-id="6eee8-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6eee8-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6eee8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6eee8-144">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6eee8-144">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6eee8-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6eee8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6eee8-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="6eee8-146">None supported</span></span><br/>                                                            |
| <span data-ttu-id="6eee8-147">標頭</span><span class="sxs-lookup"><span data-stu-id="6eee8-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eee8-148"><dt>感應器。h</dt></span><span class="sxs-lookup"><span data-stu-id="6eee8-148"><dt>Sensors.h</dt></span></span> </dl> |



 

 




