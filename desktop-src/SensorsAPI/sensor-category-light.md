---
description: '[感應器 \_ 類別] \_ 光線類別包含的感應器，可提供光線特性的相關資訊。'
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: 'SENSOR_CATEGORY_LIGHT (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847863"
---
# <a name="sensor_category_light"></a><span data-ttu-id="9ecb5-103">感應器 \_ 類別 \_ 燈</span><span class="sxs-lookup"><span data-stu-id="9ecb5-103">SENSOR\_CATEGORY\_LIGHT</span></span>

<span data-ttu-id="9ecb5-104">[感應器 \_ 類別] \_ 光線類別包含的感應器，可提供光線特性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-104">The SENSOR\_CATEGORY\_LIGHT category contains sensors that provide information about characteristics of light.</span></span>

<span data-ttu-id="9ecb5-105">**平臺定義的感應器類型**</span><span class="sxs-lookup"><span data-stu-id="9ecb5-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="9ecb5-106">此類別包括下列平臺定義的感應器類型。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="9ecb5-107">感應器類型</span><span class="sxs-lookup"><span data-stu-id="9ecb5-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="9ecb5-108">Description</span><span class="sxs-lookup"><span data-stu-id="9ecb5-108">Description</span></span>                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <span data-ttu-id="9ecb5-109"><dt>**感應器 \_輸入 \_ 環境 \_ 燈**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span><span class="sxs-lookup"><span data-stu-id="9ecb5-109"><dt>**SENSOR\_TYPE\_AMBIENT\_LIGHT**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span></span> </dl> | <span data-ttu-id="9ecb5-110">環境光線感應器。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-110">Ambient light sensors.</span></span><br/> |



<span data-ttu-id="9ecb5-111">**平臺定義的資料欄位**</span><span class="sxs-lookup"><span data-stu-id="9ecb5-111">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="9ecb5-112">此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ 光源 \_ GUID 為基礎：</span><span class="sxs-lookup"><span data-stu-id="9ecb5-112">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_LIGHT\_GUID:</span></span>

<span data-ttu-id="9ecb5-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span><span class="sxs-lookup"><span data-stu-id="9ecb5-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span></span>

<span data-ttu-id="9ecb5-114">此類別包括下列的平臺定義資料欄位。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-114">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="9ecb5-115">資料欄位名稱和 PID</span><span class="sxs-lookup"><span data-stu-id="9ecb5-115">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="9ecb5-116">Description</span><span class="sxs-lookup"><span data-stu-id="9ecb5-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <span data-ttu-id="9ecb5-117"><dt>**感應器 \_ 資料 \_ 類型 \_ LIGHT \_ CHROMACITY**</dt> <dt> (PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="9ecb5-117"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_CHROMACITY** </dt> <dt> (PID = 4) </dt></span></span> </dl>                     | <span data-ttu-id="9ecb5-118">**VT \_ 向量 \| vt \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="9ecb5-118">**VT\_VECTOR\|VT\_UI1**</span></span><br/> <span data-ttu-id="9ecb5-119">Chromaticity 為 float 值的計數陣列。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-119">Chromaticity as a counted array of float values.</span></span><br/> <span data-ttu-id="9ecb5-120">向量類型的資料一律會序列化為 **VT \_ UI1** (不帶正負號的1位元組字元陣列) 。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-120">Data for vector types is always serialized as **VT\_UI1** (an array of unsigned, 1-byte characters).</span></span> <span data-ttu-id="9ecb5-121">此資料欄位實際上包含每個值做為 IEEE 4 位元組真正值 (**VT \_ R4**) 。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-121">This data field actually contains each value as an IEEE 4-byte real value (**VT\_R4**).</span></span><br/> <span data-ttu-id="9ecb5-122">如需使用陣列的詳細資訊，請參閱抓取 [向量類型](retrieving-vector-types.md)。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-122">For information about working with arrays, see [Retrieving Vector Types](retrieving-vector-types.md).</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <span data-ttu-id="9ecb5-123"><dt>**感應器 \_資料 \_ 類型 \_ 淺 \_ 層級 \_ LUX**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="9ecb5-123"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_LEVEL\_LUX**</dt> <dt> (PID = 2) </dt></span></span> </dl>                            | <span data-ttu-id="9ecb5-124">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="9ecb5-124">**VT\_R4**</span></span><br/> <span data-ttu-id="9ecb5-125">Illuminance 層級（在 lux 中）。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-125">Illuminance level, in lux.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <span data-ttu-id="9ecb5-126"><dt>**感應器 \_資料 \_ 類型 \_ 光源 \_ 的 \_ 開氏**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="9ecb5-126"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_TEMPERATURE\_KELVIN**</dt> <dt> (PID = 3) </dt></span></span> </dl> | <span data-ttu-id="9ecb5-127">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="9ecb5-127">**VT\_R4**</span></span><br/> <span data-ttu-id="9ecb5-128">色溫，以度為單位。</span><span class="sxs-lookup"><span data-stu-id="9ecb5-128">Color temperature, in degrees Kelvin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="9ecb5-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ecb5-129">Requirements</span></span>



| <span data-ttu-id="9ecb5-130">需求</span><span class="sxs-lookup"><span data-stu-id="9ecb5-130">Requirement</span></span> | <span data-ttu-id="9ecb5-131">值</span><span class="sxs-lookup"><span data-stu-id="9ecb5-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ecb5-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ecb5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9ecb5-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ecb5-133">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9ecb5-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ecb5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9ecb5-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="9ecb5-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="9ecb5-136">標頭</span><span class="sxs-lookup"><span data-stu-id="9ecb5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ecb5-137"><dt>感應器。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ecb5-137"><dt>Sensors.h</dt></span></span> </dl> |



 

 




