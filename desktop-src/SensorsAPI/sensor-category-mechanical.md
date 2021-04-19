---
description: 感應器 \_ 類別 \_ 機械類別包含的感應器，可提供機械裝置和測量的相關資訊。
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: 'SENSOR_CATEGORY_MECHANICAL (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2446559820141b65a70bc75d25680da79563388c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972188"
---
# <a name="sensor_category_mechanical"></a><span data-ttu-id="8ec9f-103">感應器 \_ 類別 \_ 機械</span><span class="sxs-lookup"><span data-stu-id="8ec9f-103">SENSOR\_CATEGORY\_MECHANICAL</span></span>

<span data-ttu-id="8ec9f-104">感應器 \_ 類別 \_ 機械類別包含的感應器，可提供機械裝置和測量的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-104">The SENSOR\_CATEGORY\_MECHANICAL category contains sensors that provide information related to mechanical devices and measurements.</span></span>

<span data-ttu-id="8ec9f-105">**平臺定義的感應器類型**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="8ec9f-106">此類別包括下列平臺定義的感應器類型。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="8ec9f-107">感應器類型</span><span class="sxs-lookup"><span data-stu-id="8ec9f-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="8ec9f-108">Description</span><span class="sxs-lookup"><span data-stu-id="8ec9f-108">Description</span></span>                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <span data-ttu-id="8ec9f-109"><dt>**感應器 \_類型 \_ 布林值 \_ 參數**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-109"><dt>**SENSOR\_TYPE\_BOOLEAN\_SWITCH**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt></span></span> </dl>                    | <span data-ttu-id="8ec9f-110">雙狀態參數 (關閉或) 。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-110">Two-state switches (off or on).</span></span><br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <span data-ttu-id="8ec9f-111"><dt>**感應器 \_類型 \_ 布林值 \_ 參數 \_ 陣列**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-111"><dt>**SENSOR\_TYPE\_BOOLEAN\_SWITCH\_ARRAY**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt></span></span> </dl> | <span data-ttu-id="8ec9f-112">雙狀態參數的陣列 (關閉或) 。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-112">Array of two-state switches (off or on).</span></span><br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <span data-ttu-id="8ec9f-113"><dt>**感應器 \_輸入 \_ FORCE**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-113"><dt>**SENSOR\_TYPE\_FORCE**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt></span></span> </dl>                                                | <span data-ttu-id="8ec9f-114">強制感應器。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-114">Force sensors.</span></span><br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <span data-ttu-id="8ec9f-115"><dt>**感應器 \_類型多重值 \_ \_ 參數**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-115"><dt>**SENSOR\_TYPE\_MULTIVALUE\_SWITCH**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt></span></span> </dl>           | <span data-ttu-id="8ec9f-116">多重位置切換。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-116">Multiple-position switches.</span></span><br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <span data-ttu-id="8ec9f-117"><dt>**感應器 \_類型 \_ 壓力**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-117"><dt>**SENSOR\_TYPE\_PRESSURE**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt></span></span> </dl>                                       | <span data-ttu-id="8ec9f-118">壓力感應器。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-118">Pressure sensors.</span></span><br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <span data-ttu-id="8ec9f-119"><dt>**感應器 \_類型 \_ SCALE**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-119"><dt>**SENSOR\_TYPE\_SCALE**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt></span></span> </dl>                                                | <span data-ttu-id="8ec9f-120">加權感應器。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-120">Weight sensors.</span></span><br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <span data-ttu-id="8ec9f-121"><dt>**感應器 \_輸入 \_ 壓力**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-121"><dt>**SENSOR\_TYPE\_STRAIN**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt></span></span> </dl>                                             | <span data-ttu-id="8ec9f-122">減輕感應器。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-122">Strain sensors.</span></span><br/>                          |



<span data-ttu-id="8ec9f-123">**平臺定義的資料欄位**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-123">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="8ec9f-124">此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ guid \_ 機械 \_ guid 為基礎：</span><span class="sxs-lookup"><span data-stu-id="8ec9f-124">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_GUID\_MECHANICAL\_GUID:</span></span>

<span data-ttu-id="8ec9f-125">{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}</span><span class="sxs-lookup"><span data-stu-id="8ec9f-125">{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}</span></span>

<span data-ttu-id="8ec9f-126">此類別包括下列的平臺定義資料欄位。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-126">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="8ec9f-127">資料欄位名稱和 PID</span><span class="sxs-lookup"><span data-stu-id="8ec9f-127">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="8ec9f-128">Description</span><span class="sxs-lookup"><span data-stu-id="8ec9f-128">Description</span></span>                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <span data-ttu-id="8ec9f-129"><dt>**感應器 \_資料 \_ 類型 \_ 絕對 \_ 壓力 \_ PASCAL**</dt> <dt> (PID = 5)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-129"><dt>**SENSOR\_DATA\_TYPE\_ABSOLUTE\_PRESSURE\_PASCAL**</dt> <dt> (PID = 5) </dt></span></span> </dl>          | <span data-ttu-id="8ec9f-130">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-130">**VT\_R8**</span></span><br/> <span data-ttu-id="8ec9f-131">帕斯卡中的絕對壓力。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-131">Absolute pressure, in pascals.</span></span><br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <span data-ttu-id="8ec9f-132"><dt>**感應器 \_資料 \_ 類型 \_ 布林值 \_ SWITCH \_ 陣列 \_ 狀態**</dt> <dt> (PID = 10)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-132"><dt>**SENSOR\_DATA\_TYPE\_BOOLEAN\_SWITCH\_ARRAY\_STATES**</dt> <dt>(PID = 10)</dt></span></span> </dl> | <span data-ttu-id="8ec9f-133">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-133">**VT\_UI4**</span></span><br/> <span data-ttu-id="8ec9f-134">布林值參數陣列的狀態欄位。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-134">State fields for an array of Boolean switches.</span></span><br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <span data-ttu-id="8ec9f-135"><dt>**感應器 \_資料 \_ 類型 \_ 布林值 \_ 切換 \_ 狀態**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-135"><dt>**SENSOR\_DATA\_TYPE\_BOOLEAN\_SWITCH\_STATE**</dt> <dt>(PID = 2) </dt></span></span> </dl>                       | <span data-ttu-id="8ec9f-136">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-136">**VT\_BOOL**</span></span><br/> <span data-ttu-id="8ec9f-137">感應器 \_ 類型 \_ 布林值參數的狀態欄位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-137">State field for SENSOR\_TYPE\_BOOLEAN\_SWITCH.</span></span><br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <span data-ttu-id="8ec9f-138"><dt>**感應器 \_資料 \_ 類型 \_ FORCE \_ NEWTONS**</dt> <dt> (PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-138"><dt>**SENSOR\_DATA\_TYPE\_FORCE\_NEWTONS**</dt> <dt> (PID = 4) </dt></span></span> </dl>                                            | <span data-ttu-id="8ec9f-139">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-139">**VT\_R8**</span></span><br/> <span data-ttu-id="8ec9f-140">在 newtons 中強制執行。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-140">Force, in newtons.</span></span><br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <span data-ttu-id="8ec9f-141"><dt>**感應器 \_資料類型量測計 \_ \_ \_ 壓力 \_ PASCAL**</dt> <dt> (PID = 6)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-141"><dt>**SENSOR\_DATA\_TYPE\_GAUGE\_PRESSURE\_PASCAL**</dt> <dt> (PID = 6) </dt></span></span> </dl>                   | <span data-ttu-id="8ec9f-142">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-142">**VT\_R8**</span></span><br/> <span data-ttu-id="8ec9f-143">相對量測計壓力，以帕斯卡。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-143">Relative gauge pressure, in pascals.</span></span><br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <span data-ttu-id="8ec9f-144"><dt>**感應器 \_資料 \_ 類型多值 \_ \_ 切換 \_ 狀態**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-144"><dt>**SENSOR\_DATA\_TYPE\_MULTIVALUE\_SWITCH\_STATE**</dt> <dt> (PID = 3) </dt></span></span> </dl>             | <span data-ttu-id="8ec9f-145">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-145">**VT\_R8**</span></span><br/> <span data-ttu-id="8ec9f-146">感應器類型多重值參數的狀態欄位 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-146">State field for SENSOR\_TYPE\_MULTIVALUE\_SWITCH.</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <span data-ttu-id="8ec9f-147"><dt>**感應器 \_資料 \_ 類型 \_ 負擔**</dt> <dt> (PID = 7)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-147"><dt>**SENSOR\_DATA\_TYPE\_STRAIN**</dt> <dt> (PID = 7) </dt></span></span> </dl>                                                                  | <span data-ttu-id="8ec9f-148">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-148">**VT\_R8**</span></span><br/> <span data-ttu-id="8ec9f-149">應變。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-149">Strain.</span></span><br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <span data-ttu-id="8ec9f-150"><dt>**感應器 \_資料 \_ 類型 \_ 權數 \_ 公斤**</dt> <dt> (PID = 8)</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-150"><dt>**SENSOR\_DATA\_TYPE\_WEIGHT\_KILOGRAMS**</dt> <dt> (PID = 8) </dt></span></span> </dl>                                   | <span data-ttu-id="8ec9f-151">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-151">**VT\_R8**</span></span><br/> <span data-ttu-id="8ec9f-152">權數，以公斤為限。</span><span class="sxs-lookup"><span data-stu-id="8ec9f-152">Weight, in kilograms.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="8ec9f-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ec9f-153">Requirements</span></span>



| <span data-ttu-id="8ec9f-154">需求</span><span class="sxs-lookup"><span data-stu-id="8ec9f-154">Requirement</span></span> | <span data-ttu-id="8ec9f-155">值</span><span class="sxs-lookup"><span data-stu-id="8ec9f-155">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec9f-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ec9f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec9f-157">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ec9f-157">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8ec9f-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ec9f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec9f-159">都不支援</span><span class="sxs-lookup"><span data-stu-id="8ec9f-159">None supported</span></span><br/>                                                            |
| <span data-ttu-id="8ec9f-160">標頭</span><span class="sxs-lookup"><span data-stu-id="8ec9f-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec9f-161"><dt>感應器。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec9f-161"><dt>Sensors.h</dt></span></span> </dl> |



 

 




