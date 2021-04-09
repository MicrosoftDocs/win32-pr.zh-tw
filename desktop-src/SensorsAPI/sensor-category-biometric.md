---
description: 感應器 \_ 類別 \_ 生物特徵辨識類別包含的感應器，可提供客廳的相關資訊。
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: 'SENSOR_CATEGORY_BIOMETRIC (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112629"
---
# <a name="sensor_category_biometric"></a><span data-ttu-id="f371a-103">感應器 \_ 類別 \_ 生物特徵辨識</span><span class="sxs-lookup"><span data-stu-id="f371a-103">SENSOR\_CATEGORY\_BIOMETRIC</span></span>

<span data-ttu-id="f371a-104">感應器 \_ 類別 \_ 生物特徵辨識類別包含的感應器，可提供客廳的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f371a-104">The SENSOR\_CATEGORY\_BIOMETRIC category contains sensors that provide information about living beings.</span></span>

<span data-ttu-id="f371a-105">**平臺定義的感應器類型**</span><span class="sxs-lookup"><span data-stu-id="f371a-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="f371a-106">此類別包括下列平臺定義的感應器類型。</span><span class="sxs-lookup"><span data-stu-id="f371a-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="f371a-107">感應器類型</span><span class="sxs-lookup"><span data-stu-id="f371a-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="f371a-108">Description</span><span class="sxs-lookup"><span data-stu-id="f371a-108">Description</span></span>                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <span data-ttu-id="f371a-109"><dt>**感應器 \_輸入 \_ 人類 \_ 狀態**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span><span class="sxs-lookup"><span data-stu-id="f371a-109"><dt>**SENSOR\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span></span> </dl>    | <span data-ttu-id="f371a-110">偵測人為存在的感應器。</span><span class="sxs-lookup"><span data-stu-id="f371a-110">Sensors that detect human presence.</span></span><br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <span data-ttu-id="f371a-111"><dt>**感應器 \_輸入 \_ 人類 \_ 鄰近**</dt>性 <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span><span class="sxs-lookup"><span data-stu-id="f371a-111"><dt>**SENSOR\_TYPE\_HUMAN\_PROXIMITY**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span></span> </dl> | <span data-ttu-id="f371a-112">偵測人類附近的感應器。</span><span class="sxs-lookup"><span data-stu-id="f371a-112">Sensors that detect human proximity.</span></span><br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <span data-ttu-id="f371a-113"><dt>**感應器 \_輸入 \_ TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span><span class="sxs-lookup"><span data-stu-id="f371a-113"><dt>**SENSOR\_TYPE\_TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span></span> </dl>                                | <span data-ttu-id="f371a-114">觸控感應器。</span><span class="sxs-lookup"><span data-stu-id="f371a-114">Touch sensors.</span></span><br/>                       |



<span data-ttu-id="f371a-115">**平臺定義的資料欄位**</span><span class="sxs-lookup"><span data-stu-id="f371a-115">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="f371a-116">此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ 生物特徵辨識 GUID \_ 為基礎：</span><span class="sxs-lookup"><span data-stu-id="f371a-116">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_BIOMETRIC\_GUID:</span></span>

<span data-ttu-id="f371a-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span><span class="sxs-lookup"><span data-stu-id="f371a-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span></span>

<span data-ttu-id="f371a-118">此類別包括下列的平臺定義資料欄位。</span><span class="sxs-lookup"><span data-stu-id="f371a-118">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="f371a-119">資料欄位名稱和 PID</span><span class="sxs-lookup"><span data-stu-id="f371a-119">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="f371a-120">Description</span><span class="sxs-lookup"><span data-stu-id="f371a-120">Description</span></span>                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <span data-ttu-id="f371a-121"><dt>**感應器 \_資料 \_ 類型的 \_ 人為 \_ 存在**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="f371a-121"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>(PID = 2) </dt></span></span> </dl>                          | <span data-ttu-id="f371a-122">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="f371a-122">**VT\_BOOL**</span></span><br/> <span data-ttu-id="f371a-123">當人類使用電腦時 **為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f371a-123">**TRUE** when a human is using the computer.</span></span><br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <span data-ttu-id="f371a-124"><dt>**感應器 \_資料 \_ 類型的 \_ 人類 \_ 近距離 \_ 計量**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="f371a-124"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PROXIMITY\_METERS**</dt> <dt>(PID = 3) </dt></span></span> </dl> | <span data-ttu-id="f371a-125">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="f371a-125">**VT\_R4**</span></span><br/> <span data-ttu-id="f371a-126">人類和電腦之間的距離（以計量為單位）。</span><span class="sxs-lookup"><span data-stu-id="f371a-126">Distance between a human and the computer, in meters.</span></span><br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <span data-ttu-id="f371a-127"><dt>**感應器 \_資料 \_ 類型 \_ 觸控 \_ 狀態**</dt> <dt> (PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="f371a-127"><dt>**SENSOR\_DATA\_TYPE\_TOUCH\_STATE**</dt> <dt>(PID = 4) </dt></span></span> </dl>                                   | <span data-ttu-id="f371a-128">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="f371a-128">**VT\_BOOL**</span></span><br/> <span data-ttu-id="f371a-129">觸碰觸控感應器時為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f371a-129">**TRUE** when the touch sensor is being touched; otherwise, **FALSE**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f371a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f371a-130">Requirements</span></span>



| <span data-ttu-id="f371a-131">需求</span><span class="sxs-lookup"><span data-stu-id="f371a-131">Requirement</span></span> | <span data-ttu-id="f371a-132">值</span><span class="sxs-lookup"><span data-stu-id="f371a-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f371a-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f371a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f371a-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f371a-134">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f371a-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f371a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f371a-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="f371a-136">None supported</span></span><br/>                                                            |
| <span data-ttu-id="f371a-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f371a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f371a-138"><dt>感應器。h</dt></span><span class="sxs-lookup"><span data-stu-id="f371a-138"><dt>Sensors.h</dt></span></span> </dl> |



 

 




