---
description: Windows 映像取得 (WIA) 硬體裝置具有儲存在 Windows 登錄中的屬性值。 如需詳細資訊，請參閱一般裝置屬性常數。
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: '攝影機裝置屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469108"
---
# <a name="camera-device-property-constants"></a><span data-ttu-id="26979-104">攝影機裝置屬性常數</span><span class="sxs-lookup"><span data-stu-id="26979-104">Camera Device Property Constants</span></span>

<span data-ttu-id="26979-105">Windows 映像取得 (WIA) 硬體裝置具有儲存在 Windows 登錄中的屬性值。</span><span class="sxs-lookup"><span data-stu-id="26979-105">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="26979-106">如需詳細資訊，請參閱 [**一般裝置屬性常數**](-wia-wiaitempropcommondevice.md)。</span><span class="sxs-lookup"><span data-stu-id="26979-106">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span>

<span data-ttu-id="26979-107">下列裝置屬性常數（與其相關聯的字串）是數位相機專用的。</span><span class="sxs-lookup"><span data-stu-id="26979-107">The following device property constants, with their associated strings, are specific to digital cameras.</span></span> <span data-ttu-id="26979-108">前置詞 "WIA \_ DPC \_ " 表示相機的裝置屬性，而且是 C/c + + 中使用的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="26979-108">The prefix "WIA\_DPC\_" indicates a Device Property for Cameras and is the naming convention used in C/C++.</span></span> <span data-ttu-id="26979-109">針對腳本用途，這些常數會使用前置詞 "CameraDevice"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。</span><span class="sxs-lookup"><span data-stu-id="26979-109">For scripting purposes these constants use the prefix "CameraDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="26979-110">來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。</span><span class="sxs-lookup"><span data-stu-id="26979-110">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="26979-111">WIA 不支援 Windows Vista 或更新版本中的相機。</span><span class="sxs-lookup"><span data-stu-id="26979-111">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="26979-112">針對這些版本的 Windows，請使用 Windows 驅動程式開發工具組中所述的 Windows 可攜式裝置 (WPD) API (DDK) 從相機取得映射。</span><span class="sxs-lookup"><span data-stu-id="26979-112">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="26979-113">常數/值</span><span class="sxs-lookup"><span data-stu-id="26979-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="26979-114">Description</span><span class="sxs-lookup"><span data-stu-id="26979-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <span data-ttu-id="26979-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26979-116">相機拍攝的圖片數目。</span><span class="sxs-lookup"><span data-stu-id="26979-116">The number of pictures that the camera has taken.</span></span> <span data-ttu-id="26979-117">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="26979-117">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="26979-118">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-118">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <span data-ttu-id="26979-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26979-120">給定目前的屬性設定，可取得的圖片數目。</span><span class="sxs-lookup"><span data-stu-id="26979-120">The number of pictures that can be taken, given the current property settings.</span></span> <span data-ttu-id="26979-121">如果這些設定變更，而變更影響相機裝置產生的影像大小，則 WIA 迷你驅動程式應該會更新剩餘的圖片數目。</span><span class="sxs-lookup"><span data-stu-id="26979-121">If these settings change, and the changes affect the size of the images that the camera device produces, the WIA minidriver should update the number of remaining pictures.</span></span> <span data-ttu-id="26979-122">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="26979-122">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="26979-123">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-123">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <span data-ttu-id="26979-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="26979-125">指出相機目前的曝光模式。</span><span class="sxs-lookup"><span data-stu-id="26979-125">Indicates the camera's current exposure mode.</span></span> <span data-ttu-id="26979-126">應用程式會變更這個屬性，以控制攝影機裝置的曝光模式。</span><span class="sxs-lookup"><span data-stu-id="26979-126">An application changes this property to control the exposure mode of the camera device.</span></span><br/> <span data-ttu-id="26979-127">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-127">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="26979-128">下表包含七個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="26979-128">The following table has the seven constants that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-129">曝光模式</span><span class="sxs-lookup"><span data-stu-id="26979-129">Exposure Mode</span></span></th>
<th><span data-ttu-id="26979-130">Description</span><span class="sxs-lookup"><span data-stu-id="26979-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-131">EXPOSUREMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="26979-131">EXPOSUREMODE_MANUAL</span></span></td>
<td><span data-ttu-id="26979-132">快門速度和光圈是由使用者設定。</span><span class="sxs-lookup"><span data-stu-id="26979-132">The shutter speed and aperture are set by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-133">EXPOSUREMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="26979-133">EXPOSUREMODE_AUTO</span></span></td>
<td><span data-ttu-id="26979-134">攝影機會自動設定快門速度和光圈。</span><span class="sxs-lookup"><span data-stu-id="26979-134">The shutter speed and aperture are automatically set by the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-135">EXPOSUREMODE_APERTURE_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="26979-135">EXPOSUREMODE_APERTURE_PRIORITY</span></span></td>
<td><span data-ttu-id="26979-136">光圈是由使用者設定，而相機會自動設定快門速度。</span><span class="sxs-lookup"><span data-stu-id="26979-136">The aperture is set by the user, and the camera automatically sets the shutter speed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-137">EXPOSUREMODE_SHUTTER_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="26979-137">EXPOSUREMODE_SHUTTER_PRIORITY</span></span></td>
<td><span data-ttu-id="26979-138">快門速度是由使用者設定，而相機會自動設定光圈。</span><span class="sxs-lookup"><span data-stu-id="26979-138">The shutter speed is set by the user, and the camera automatically sets the aperture.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-139">EXPOSUREMODE_PROGRAM_CREATIVE</span><span class="sxs-lookup"><span data-stu-id="26979-139">EXPOSUREMODE_PROGRAM_CREATIVE</span></span></td>
<td><span data-ttu-id="26979-140">攝影機會自動設定快門速度和光圈，並針對仍有主題的優化。</span><span class="sxs-lookup"><span data-stu-id="26979-140">The shutter speed and aperture are automatically set by the camera, optimized for still subject matter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-141">EXPOSUREMODE_PROGRAM_ACTION</span><span class="sxs-lookup"><span data-stu-id="26979-141">EXPOSUREMODE_PROGRAM_ACTION</span></span></td>
<td><span data-ttu-id="26979-142">攝影機會自動設定快門速度和光圈，並針對包含快速運動的場景進行優化。</span><span class="sxs-lookup"><span data-stu-id="26979-142">The shutter speed and aperture are automatically set by the camera, optimized for scenes containing fast motion.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-143">EXPOSUREMODE_PORTRAIT</span><span class="sxs-lookup"><span data-stu-id="26979-143">EXPOSUREMODE_PORTRAIT</span></span></td>
<td><span data-ttu-id="26979-144">攝影機會自動設定快門速度和光圈，並針對直向攝影進行優化。</span><span class="sxs-lookup"><span data-stu-id="26979-144">The shutter speed and aperture are automatically set by the camera, optimized for portrait photography.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <span data-ttu-id="26979-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-146">允許調整數位相機自動曝光控制的設定點。</span><span class="sxs-lookup"><span data-stu-id="26979-146">Allows for the adjustment of the set point of the digital camera's auto-exposure control.</span></span> <span data-ttu-id="26979-147">例如，設定為零不會變更原廠設定的自動曝光層級。</span><span class="sxs-lookup"><span data-stu-id="26979-147">For example, a setting of zero does not change the factory-set auto-exposure level.</span></span> <span data-ttu-id="26979-148">單位會在以 &quot; &quot; 1000 因數調整的停止，以允許小數停止值。</span><span class="sxs-lookup"><span data-stu-id="26979-148">The units are in &quot;stops&quot; that are scaled by a factor of 1000, to allow for fractional stop values.</span></span> <span data-ttu-id="26979-149">2000的設定會對應到兩個 (停止更多的曝光四倍的感應器) 的能源，產生較亮的影像。</span><span class="sxs-lookup"><span data-stu-id="26979-149">A setting of 2000 corresponds to two stops more exposure (four times more energy on the sensor), yielding brighter images.</span></span> <span data-ttu-id="26979-150">若設定為-1000，則會對應至一個低度的 (，感應器的一半能源) 產生較暗的影像。</span><span class="sxs-lookup"><span data-stu-id="26979-150">A setting of -1000 corresponds to one stop less exposure (one-half the energy on the sensor) yielding darker images.</span></span> <span data-ttu-id="26979-151">設定值是在影像曝光的加法系統中 (頂點) 單位。</span><span class="sxs-lookup"><span data-stu-id="26979-151">The setting values are in Additive System of Photographic Exposure (APEX) units.</span></span> <span data-ttu-id="26979-152">這個屬性可以表示為清單或值範圍。</span><span class="sxs-lookup"><span data-stu-id="26979-152">This property may be expressed as either a list or a range of values.</span></span> <span data-ttu-id="26979-153">只有當裝置將 <strong>WIA_DPC_EXPOSURE_MODE</strong> 屬性設定為 EXPOSUREMODE_MANUAL 時，才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="26979-153">This property is typically used only when the device has the <strong>WIA_DPC_EXPOSURE_MODE</strong> property set to EXPOSUREMODE_MANUAL.</span></span></p>
<p><span data-ttu-id="26979-154">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 或 WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="26979-154">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <span data-ttu-id="26979-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-156">對應于依10000調整的快門速度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="26979-156">Corresponds to the shutter speed, in seconds that are scaled by 10,000.</span></span> <span data-ttu-id="26979-157">通常，只有當 <strong>WIA_DPC_EXPOSURE_MODE</strong> 屬性設定為 EXPOSUREMODE_MANUAL 或 EXPOSUREMODE_SHUTTER_PRIORITY 時，裝置才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="26979-157">Typically, the device uses this property only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_SHUTTER_PRIORITY.</span></span></p>
<p><span data-ttu-id="26979-158">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 或 WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="26979-158">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <span data-ttu-id="26979-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-160">對應至鏡頭的光圈，以 f-停止數位的單位來調整100。</span><span class="sxs-lookup"><span data-stu-id="26979-160">Corresponds to the aperture of the lens, in units of the f-stop number scaled by 100.</span></span> <span data-ttu-id="26979-161">這個屬性的設定通常只有當 <strong>WIA_DPC_EXPOSURE_MODE</strong> 屬性設定為 EXPOSUREMODE_MANUAL 或 EXPOSUREMODE_APERTURE_PRIORITY 時才有效。</span><span class="sxs-lookup"><span data-stu-id="26979-161">The setting of this property is typically valid only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_APERTURE_PRIORITY.</span></span></p>
<p><span data-ttu-id="26979-162">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-162">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <span data-ttu-id="26979-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-164">定義相機裝置的目前閃爍模式設定。</span><span class="sxs-lookup"><span data-stu-id="26979-164">Defines the current flash mode setting for the camera device.</span></span> <span data-ttu-id="26979-165">設備磁碟機會列舉這個屬性支援的值。</span><span class="sxs-lookup"><span data-stu-id="26979-165">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="26979-166">應用程式會寫入此屬性，以設定相機裝置的閃爍模式。</span><span class="sxs-lookup"><span data-stu-id="26979-166">An application writes this property to set the flash mode for the camera device.</span></span></p>
<p><span data-ttu-id="26979-167">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-167">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="26979-168">下表包含六個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="26979-168">The following table has the six constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-169">Flash 模式</span><span class="sxs-lookup"><span data-stu-id="26979-169">Flash Mode</span></span></th>
<th><span data-ttu-id="26979-170">定義</span><span class="sxs-lookup"><span data-stu-id="26979-170">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-171">FLASHMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="26979-171">FLASHMODE_AUTO</span></span></td>
<td><span data-ttu-id="26979-172">攝影機裝置決定適當的閃爍設定。</span><span class="sxs-lookup"><span data-stu-id="26979-172">The camera device determines the proper flash settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-173">FLASHMODE_FILL</span><span class="sxs-lookup"><span data-stu-id="26979-173">FLASHMODE_FILL</span></span></td>
<td><span data-ttu-id="26979-174">無論目前的光源條件為何，相機裝置都會設定為 flash。</span><span class="sxs-lookup"><span data-stu-id="26979-174">The camera device is configured to flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-175">FLASHMODE_OFF</span><span class="sxs-lookup"><span data-stu-id="26979-175">FLASHMODE_OFF</span></span></td>
<td><span data-ttu-id="26979-176">攝影機裝置設定為 <em>不</em> 會針對拍攝的任何圖片進行閃爍。</span><span class="sxs-lookup"><span data-stu-id="26979-176">The camera device is configured <em>not</em> to flash for any picture taken.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-177">FLASHMODE_REDEYE_AUTO</span><span class="sxs-lookup"><span data-stu-id="26979-177">FLASHMODE_REDEYE_AUTO</span></span></td>
<td><span data-ttu-id="26979-178">攝影機裝置會使用紅眼減少來決定適當的閃光燈設定，不論目前的光源條件為何。</span><span class="sxs-lookup"><span data-stu-id="26979-178">The camera device determines the proper flash settings using red-eye reduction, regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-179">FLASHMODE_REDEYE_FILL</span><span class="sxs-lookup"><span data-stu-id="26979-179">FLASHMODE_REDEYE_FILL</span></span></td>
<td><span data-ttu-id="26979-180">無論目前的光源條件為何，相機裝置都會設定為使用紅眼降低和閃爍。</span><span class="sxs-lookup"><span data-stu-id="26979-180">The camera device is configured to use red-eye reduction and flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-181">FLASHMODE_EXTERNALSYNC</span><span class="sxs-lookup"><span data-stu-id="26979-181">FLASHMODE_EXTERNALSYNC</span></span></td>
<td><span data-ttu-id="26979-182">攝影機裝置設定為與外部 flash 單位進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="26979-182">The camera device is configured to synchronize with external flash units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <span data-ttu-id="26979-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-184">定義相機裝置的目前焦點模式設定。</span><span class="sxs-lookup"><span data-stu-id="26979-184">Defines the current focus mode setting for the camera device.</span></span> <span data-ttu-id="26979-185">設備磁碟機會列舉這個屬性支援的值。</span><span class="sxs-lookup"><span data-stu-id="26979-185">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="26979-186">應用程式會寫入這個屬性，以設定相機裝置的焦點模式。</span><span class="sxs-lookup"><span data-stu-id="26979-186">An application writes this property to set the focus mode for the camera device.</span></span></p>
<p><span data-ttu-id="26979-187">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-187">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="26979-188">下表有三個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="26979-188">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-189">焦點模式</span><span class="sxs-lookup"><span data-stu-id="26979-189">Focus Mode</span></span></th>
<th><span data-ttu-id="26979-190">Description</span><span class="sxs-lookup"><span data-stu-id="26979-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-191">FOCUSMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="26979-191">FOCUSMODE_MANUAL</span></span></td>
<td><span data-ttu-id="26979-192">攝影機裝置已設定為允許使用者以手動方式進行焦點。</span><span class="sxs-lookup"><span data-stu-id="26979-192">The camera device is configured to allow the user to focus manually.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-193">FOCUSMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="26979-193">FOCUSMODE_AUTO</span></span></td>
<td><span data-ttu-id="26979-194">攝影機裝置設定為自動焦點。</span><span class="sxs-lookup"><span data-stu-id="26979-194">The camera device is configured to focus automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-195">FOCUSMODE_MACROAUTO</span><span class="sxs-lookup"><span data-stu-id="26979-195">FOCUSMODE_MACROAUTO</span></span></td>
<td><span data-ttu-id="26979-196">攝影機裝置已設定為使用短範圍宏設定自動焦點。</span><span class="sxs-lookup"><span data-stu-id="26979-196">The camera device is configured to focus automatically using short-range macro settings.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <span data-ttu-id="26979-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26979-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-198">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="26979-198">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="26979-199">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-199">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <span data-ttu-id="26979-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26979-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-201">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="26979-201">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="26979-202">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-202">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <span data-ttu-id="26979-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-204">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="26979-204">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="26979-205">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <span data-ttu-id="26979-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-207">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="26979-207">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="26979-208">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-208">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <span data-ttu-id="26979-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-210">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="26979-210">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="26979-211">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-211">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <span data-ttu-id="26979-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-213">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="26979-213">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="26979-214">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-214">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <span data-ttu-id="26979-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-216">定義相機裝置目前的電源來源。</span><span class="sxs-lookup"><span data-stu-id="26979-216">Defines the current power source for the camera device.</span></span> <span data-ttu-id="26979-217">應用程式會讀取此屬性，以決定相機使用的電源來源。</span><span class="sxs-lookup"><span data-stu-id="26979-217">An application reads this property to determine what power source the camera is using.</span></span></p>
<p><span data-ttu-id="26979-218">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-218">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="26979-219">下表有兩個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="26979-219">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-220">電源模式</span><span class="sxs-lookup"><span data-stu-id="26979-220">Power Mode</span></span></th>
<th><span data-ttu-id="26979-221">Description</span><span class="sxs-lookup"><span data-stu-id="26979-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-222">POWERMODE_LINE</span><span class="sxs-lookup"><span data-stu-id="26979-222">POWERMODE_LINE</span></span></td>
<td><span data-ttu-id="26979-223">攝影機裝置正在電源卡上運作。</span><span class="sxs-lookup"><span data-stu-id="26979-223">The camera device is operating on a power adapter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-224">POWERMODE_BATTERY</span><span class="sxs-lookup"><span data-stu-id="26979-224">POWERMODE_BATTERY</span></span></td>
<td><span data-ttu-id="26979-225">攝影機裝置以電池電力運作。</span><span class="sxs-lookup"><span data-stu-id="26979-225">The camera device is operating on battery power.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <span data-ttu-id="26979-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-227">用來操作相機裝置的電池電力百分比。</span><span class="sxs-lookup"><span data-stu-id="26979-227">The percentage of battery power that is left to operate the camera device.</span></span> <span data-ttu-id="26979-228">此值應該是從0到100的整數。</span><span class="sxs-lookup"><span data-stu-id="26979-228">This value should be an integer from 0 through 100.</span></span> <span data-ttu-id="26979-229">應用程式會讀取此屬性，以決定相機裝置的剩餘電池壽命。</span><span class="sxs-lookup"><span data-stu-id="26979-229">An application reads this property to determine the remaining battery life of the camera device.</span></span></p>
<p><span data-ttu-id="26979-230">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-230">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <span data-ttu-id="26979-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-232">要用於新捕獲影像的縮圖影像寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="26979-232">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="26979-233">應用程式會讀取此值，以取得在其使用者介面中顯示縮圖的估計大小。</span><span class="sxs-lookup"><span data-stu-id="26979-233">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="26979-234">類型： <strong>VT_I4</strong>、存取：讀取/寫入 (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) 或唯讀 (WIA_PROP_NONE) ，有效的值： WIA_PROP_LIST 或 WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="26979-234">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <span data-ttu-id="26979-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-236">要用於新捕獲影像的縮圖影像寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="26979-236">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="26979-237">應用程式會讀取此值，以取得在其使用者介面中顯示縮圖的估計大小。</span><span class="sxs-lookup"><span data-stu-id="26979-237">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="26979-238">類型： <strong>VT_I4</strong>、存取：讀取/寫入 (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) 或唯讀 (WIA_PROP_NONE) ，有效的值： WIA_PROP_LIST 或 WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="26979-238">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <span data-ttu-id="26979-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-240">用於新捕獲影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="26979-240">The width in pixels to use for newly captured images.</span></span> <span data-ttu-id="26979-241">這個屬性的有效值清單會與 <strong>WIA_DPC_PICT_HEIGHT</strong> 屬性的有效值清單有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="26979-241">The list of valid values for this property has a one-to-one correspondence to the list of valid values for the <strong>WIA_DPC_PICT_HEIGHT</strong> property.</span></span> <span data-ttu-id="26979-242">如果個別的寬度和高度具有線性可設定並彼此垂直，則可能會以範圍表示。</span><span class="sxs-lookup"><span data-stu-id="26979-242">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="26979-243">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-243">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <span data-ttu-id="26979-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-245">用於新捕獲影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="26979-245">The height in pixels to use for newly captured images.</span></span> <span data-ttu-id="26979-246">這個屬性的有效值清單與 <strong>WIA_DPC_PICT_WIDTH</strong> 屬性的有效值清單會有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="26979-246">The list of valid values for this property has a one-to-one correspondence with the list of valid values for the <strong>WIA_DPC_PICT_WIDTH</strong> property.</span></span> <span data-ttu-id="26979-247">如果個別的寬度和高度具有線性可設定並彼此垂直，則可能會以範圍表示。</span><span class="sxs-lookup"><span data-stu-id="26979-247">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="26979-248">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-248">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <span data-ttu-id="26979-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26979-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-250">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="26979-250">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="26979-251">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-251">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <span data-ttu-id="26979-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-253">預計在廣泛的場景內容上看到影像品質更接近線性，並且包含範圍或整數清單。</span><span class="sxs-lookup"><span data-stu-id="26979-253">Intended to be approximately linear with respect to perceived image quality over a broad range of scene content, and it contains either a range or a list of integers.</span></span> <span data-ttu-id="26979-254">使用較小的整數來表示較低的品質 (也就是最大的壓縮) ，而較大的整數則用來表示較高的品質 (也就是最小的壓縮) 。</span><span class="sxs-lookup"><span data-stu-id="26979-254">Smaller integers are used to represent lower quality (that is, maximum compression), whereas larger integers are used to represent higher quality (that is, minimum compression).</span></span> <span data-ttu-id="26979-255">裝置上的任何可用設定都是相對於該裝置，因此是裝置特定的設定。</span><span class="sxs-lookup"><span data-stu-id="26979-255">Any available settings on a device are relative only to that device and are therefore device specific.</span></span></p>
<p><span data-ttu-id="26979-256">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-256">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <span data-ttu-id="26979-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="26979-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-258">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="26979-258">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="26979-259">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-259">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <span data-ttu-id="26979-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-261">以毫秒為單位的時間，這是在時間間隔捕獲作業中的影像捕捉之間的時間。</span><span class="sxs-lookup"><span data-stu-id="26979-261">The time, in milliseconds, between image captures in a time-lapse capture operation.</span></span></p>
<p><span data-ttu-id="26979-262">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>、WIA_PROP_LIST 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-262">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <span data-ttu-id="26979-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-264">裝置在時間間隔期間嘗試捕捉的影像數目。</span><span class="sxs-lookup"><span data-stu-id="26979-264">The number of images the device attempts to capture during a time-lapse capture.</span></span></p>
<p><span data-ttu-id="26979-265">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>、WIA_PROP_LIST 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-265">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <span data-ttu-id="26979-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-267">在高載操作期間，映射捕捉之間的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="26979-267">The time, in milliseconds, between image captures during a burst operation.</span></span></p>
<p><span data-ttu-id="26979-268">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>、WIA_PROP_LIST 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-268">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <span data-ttu-id="26979-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-270">裝置在高載作業期間嘗試捕獲的影像數目。</span><span class="sxs-lookup"><span data-stu-id="26979-270">The number of images the device attempts to capture during a burst operation.</span></span></p>
<p><span data-ttu-id="26979-271">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>、WIA_PROP_LIST 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-271">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <span data-ttu-id="26979-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-273">指定相機的特殊影像取得模式。</span><span class="sxs-lookup"><span data-stu-id="26979-273">Specifies the special image acquisition mode of the camera.</span></span></p>
<p><span data-ttu-id="26979-274">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-274">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="26979-275">下表有三個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="26979-275">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-276">效果模式</span><span class="sxs-lookup"><span data-stu-id="26979-276">Effect Mode</span></span></th>
<th><span data-ttu-id="26979-277">Description</span><span class="sxs-lookup"><span data-stu-id="26979-277">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-278">EFFECTMODE_STANDARD</span><span class="sxs-lookup"><span data-stu-id="26979-278">EFFECTMODE_STANDARD</span></span></td>
<td><span data-ttu-id="26979-279">使用相機的標準模式來捕捉映射。</span><span class="sxs-lookup"><span data-stu-id="26979-279">Capture an image in the standard mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-280">EFFECTMODE_BW</span><span class="sxs-lookup"><span data-stu-id="26979-280">EFFECTMODE_BW</span></span></td>
<td><span data-ttu-id="26979-281">捕捉灰階影像。</span><span class="sxs-lookup"><span data-stu-id="26979-281">Capture a grayscale image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-282">EFFECTMODE_SEPIA</span><span class="sxs-lookup"><span data-stu-id="26979-282">EFFECTMODE_SEPIA</span></span></td>
<td><span data-ttu-id="26979-283">捕獲棕褐色的影像。</span><span class="sxs-lookup"><span data-stu-id="26979-283">Capture a sepia image.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <span data-ttu-id="26979-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-285">數位相機取得之影像的有效縮放比例，以10倍的比例進行縮放。</span><span class="sxs-lookup"><span data-stu-id="26979-285">The effective zoom ratio of the digital camera's acquired image, scaled by a factor of 10.</span></span> <span data-ttu-id="26979-286">10的值對應于缺少數位縮放 (1X) ，也就是相機所捕捉的標準場景大小。</span><span class="sxs-lookup"><span data-stu-id="26979-286">A value of 10 corresponds to the absence of digital zoom (1X), which is the standard scene size captured by the camera.</span></span> <span data-ttu-id="26979-287">值為20時，會對應至2X 縮放，其中一季的標準場景大小是由相機所捕捉。</span><span class="sxs-lookup"><span data-stu-id="26979-287">A value of 20 corresponds to a 2X zoom, where one-quarter of the standard scene size is captured by the camera.</span></span></p>
<p><span data-ttu-id="26979-288">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-288">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <span data-ttu-id="26979-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-290">所捕捉影像的已察覺清晰度。</span><span class="sxs-lookup"><span data-stu-id="26979-290">The perceived sharpness of a captured image.</span></span> <span data-ttu-id="26979-291">這個屬性可以使用值清單或值範圍。</span><span class="sxs-lookup"><span data-stu-id="26979-291">This property can use either a list of values or a range of values.</span></span> <span data-ttu-id="26979-292">最小值代表最少的清晰度，而最大值代表最大清晰度。</span><span class="sxs-lookup"><span data-stu-id="26979-292">The minimum value represents the least amount of sharpness, whereas the maximum value represents the maximum sharpness.</span></span> <span data-ttu-id="26979-293">通常範圍中間的值代表一般或預設的清晰度。</span><span class="sxs-lookup"><span data-stu-id="26979-293">Typically a value in the middle of the range represents normal, or default, sharpness.</span></span></p>
<p><span data-ttu-id="26979-294">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-294">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <span data-ttu-id="26979-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-296">已捕捉的映射已察覺對比。</span><span class="sxs-lookup"><span data-stu-id="26979-296">The perceived contrast of a captured image.</span></span> <span data-ttu-id="26979-297">這個屬性可以包含值清單或值範圍。</span><span class="sxs-lookup"><span data-stu-id="26979-297">This property can contain either a list of values or a range of values.</span></span> <span data-ttu-id="26979-298">最小支援的值代表最小的對比，而最大值代表最高的對比。</span><span class="sxs-lookup"><span data-stu-id="26979-298">The minimum supported value represents the least amount of contrast, whereas the maximum value represents the most contrast.</span></span> <span data-ttu-id="26979-299">一般來說，範圍中間的值代表一般或預設的對比。</span><span class="sxs-lookup"><span data-stu-id="26979-299">Typically, a value in the middle of the range represents normal, or default, contrast.</span></span></p>
<p><span data-ttu-id="26979-300">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-300">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <span data-ttu-id="26979-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-302">設定影像捕捉模式。</span><span class="sxs-lookup"><span data-stu-id="26979-302">Sets the image capture mode.</span></span></p>
<p><span data-ttu-id="26979-303">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-303">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="26979-304">下表有三個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="26979-304">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-305">擷取模式</span><span class="sxs-lookup"><span data-stu-id="26979-305">Capture Mode</span></span></th>
<th><span data-ttu-id="26979-306">Description</span><span class="sxs-lookup"><span data-stu-id="26979-306">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-307">CAPTUREMODE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="26979-307">CAPTUREMODE_NORMAL</span></span></td>
<td><span data-ttu-id="26979-308">攝影機的標準模式。</span><span class="sxs-lookup"><span data-stu-id="26979-308">Normal mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-309">CAPTUREMODE_BURST</span><span class="sxs-lookup"><span data-stu-id="26979-309">CAPTUREMODE_BURST</span></span></td>
<td><span data-ttu-id="26979-310">依照 <strong>WIA_DPC_BURST_NUMBER</strong> 和 <strong>WIA_DPC_BURST_INTERVAL</strong> 屬性的值所定義，快速連續地捕捉一個以上的影像。</span><span class="sxs-lookup"><span data-stu-id="26979-310">Capture more than one image in quick succession as defined by the values of the <strong>WIA_DPC_BURST_NUMBER</strong> and <strong>WIA_DPC_BURST_INTERVAL</strong> properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-311">CAPTUREMODE_TIMELAPSE</span><span class="sxs-lookup"><span data-stu-id="26979-311">CAPTUREMODE_TIMELAPSE</span></span></td>
<td><span data-ttu-id="26979-312">依照 <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> 和 <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> 屬性的定義，連續捕捉一個以上的影像。</span><span class="sxs-lookup"><span data-stu-id="26979-312">Capture more than one image in succession as defined by the <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> properties.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <span data-ttu-id="26979-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-314">值，表示應該在捕獲觸發程式與實際初始資料捕獲之間插入的時間延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="26979-314">The value representing the amount of time delay, in milliseconds, that should be inserted between the capture trigger and the actual initiation of the data capture.</span></span> <span data-ttu-id="26979-315">這個屬性不能用來描述單一初始初始的框架之間的時間、多重捕獲（例如高載或時間間隔），其具有個別的間隔屬性 <strong>WIA_DPC_BURST_INTERVAL</strong> 和 <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>。</span><span class="sxs-lookup"><span data-stu-id="26979-315">This property is not intended to be used to describe the time between frames for single-initiation, multiple captures such as burst or time lapse, which have separate interval properties <strong>WIA_DPC_BURST_INTERVAL</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span></span> <span data-ttu-id="26979-316">在這些情況下，它仍會作為系列中第一個映射的初始延遲，與框架之間的時間無關。</span><span class="sxs-lookup"><span data-stu-id="26979-316">In those cases, it still serves as an initial delay before the first image in the series is captured, independent of the time between frames.</span></span> <span data-ttu-id="26979-317">如果沒有 precapture 延遲，此屬性應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="26979-317">For no precapture delay, this property should be set to zero.</span></span></p>
<p><span data-ttu-id="26979-318">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-318">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <span data-ttu-id="26979-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-320">允許模擬數位相機上的電影速度設定。</span><span class="sxs-lookup"><span data-stu-id="26979-320">Allows for the emulation of film speed settings on a digital camera.</span></span> <span data-ttu-id="26979-321">這些設定會對應到 (ASA/等) 的 ISO 指派。</span><span class="sxs-lookup"><span data-stu-id="26979-321">The settings correspond to the ISO designations (ASA/DIN).</span></span> <span data-ttu-id="26979-322">通常，裝置支援離散列舉值，但可能會持續控制某個範圍的值。</span><span class="sxs-lookup"><span data-stu-id="26979-322">Typically, a device supports discrete enumerated values, but continuous control over a range of values is possible.</span></span> <span data-ttu-id="26979-323">0xFFFF 的值對應到自動 ISO 設定。</span><span class="sxs-lookup"><span data-stu-id="26979-323">A value of 0xFFFF corresponds to the Automatic ISO setting.</span></span></p>
<p><span data-ttu-id="26979-324">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-324">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <span data-ttu-id="26979-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-326">指定相機用來自動調整曝光設定的模式。</span><span class="sxs-lookup"><span data-stu-id="26979-326">Specifies the mode the camera uses to automatically adjust the exposure setting.</span></span></p>
<p><span data-ttu-id="26979-327">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-327">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-328">曝光計量模式</span><span class="sxs-lookup"><span data-stu-id="26979-328">Exposure Metering Mode</span></span></th>
<th><span data-ttu-id="26979-329">Description</span><span class="sxs-lookup"><span data-stu-id="26979-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-330">EXPOSUREMETERING_AVERAGE</span><span class="sxs-lookup"><span data-stu-id="26979-330">EXPOSUREMETERING_AVERAGE</span></span></td>
<td><span data-ttu-id="26979-331">根據整個場景的平均值來設定曝光。</span><span class="sxs-lookup"><span data-stu-id="26979-331">Set the exposure based on an average of the entire scene.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-332">EXPOSUREMETERING_CENTERWEIGHT</span><span class="sxs-lookup"><span data-stu-id="26979-332">EXPOSUREMETERING_CENTERWEIGHT</span></span></td>
<td><span data-ttu-id="26979-333">根據中央加權平均設定曝光。</span><span class="sxs-lookup"><span data-stu-id="26979-333">Set the exposure based on a center-weighted average.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-334">EXPOSUREMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="26979-334">EXPOSUREMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="26979-335">設定以 multispot 模式為基礎的曝光。</span><span class="sxs-lookup"><span data-stu-id="26979-335">Set the exposure based on a multispot pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-336">EXPOSUREMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="26979-336">EXPOSUREMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="26979-337">根據中心點設定曝光。</span><span class="sxs-lookup"><span data-stu-id="26979-337">Set the exposure based on a center spot.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <span data-ttu-id="26979-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-339">指定相機用來自動調整焦點的模式。</span><span class="sxs-lookup"><span data-stu-id="26979-339">Specifies the mode the camera uses to automatically adjust the focus.</span></span></p>
<p><span data-ttu-id="26979-340">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-340">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="26979-341">下表有兩個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="26979-341">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-342">焦點計量模式</span><span class="sxs-lookup"><span data-stu-id="26979-342">Focus Metering Mode</span></span></th>
<th><span data-ttu-id="26979-343">Description</span><span class="sxs-lookup"><span data-stu-id="26979-343">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-344">FOCUSMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="26979-344">FOCUSMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="26979-345">根據中央位置調整焦點。</span><span class="sxs-lookup"><span data-stu-id="26979-345">Adjust the focus based on a center spot.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-346">FOCUSMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="26979-346">FOCUSMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="26979-347">根據 multispot 模式調整焦點。</span><span class="sxs-lookup"><span data-stu-id="26979-347">Adjust the focus based on a multispot pattern.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <span data-ttu-id="26979-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-349">數位相機的影像捕捉平面和焦點點之間的距離（以毫米為單位）。</span><span class="sxs-lookup"><span data-stu-id="26979-349">The distance, in millimeters, between the image-capturing plane of the digital camera and the point of focus.</span></span> <span data-ttu-id="26979-350">0xFFFF 的值對應到大於655計量的設定。</span><span class="sxs-lookup"><span data-stu-id="26979-350">A value of 0xFFFF corresponds to a setting greater than 655 meters.</span></span></p>
<p><span data-ttu-id="26979-351">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="26979-351">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <span data-ttu-id="26979-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-353">35mm 對等的焦長度。</span><span class="sxs-lookup"><span data-stu-id="26979-353">The 35mm-equivalent focal length.</span></span> <span data-ttu-id="26979-354">這個屬性的值會對應到以毫米乘以100的焦距長度。</span><span class="sxs-lookup"><span data-stu-id="26979-354">The values of this property correspond to the focal length in millimeters multiplied by 100.</span></span> <span data-ttu-id="26979-355">焦長度會決定光學縮放。</span><span class="sxs-lookup"><span data-stu-id="26979-355">The focal length determines the optical zoom.</span></span></p>
<p><span data-ttu-id="26979-356">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-356">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <span data-ttu-id="26979-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-358">以 null 終止的 Unicode 字串，表示分別套用至影像資料的紅色、綠色和藍色增益。</span><span class="sxs-lookup"><span data-stu-id="26979-358">A null-terminated Unicode string that represents the red, green, and blue gain applied to image data, respectively.</span></span> <span data-ttu-id="26979-359">例如， &quot; 4:25:50 &quot; 代表紅色增益4、有25的綠色增益，以及50的藍色增益。</span><span class="sxs-lookup"><span data-stu-id="26979-359">For example, &quot;4:25:50&quot; represents a red gain of 4, a green gain of 25, and a blue gain of 50.</span></span></p>
<p><span data-ttu-id="26979-360">Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-360">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <span data-ttu-id="26979-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-362">指定數位相機加權色頻。</span><span class="sxs-lookup"><span data-stu-id="26979-362">Specifies how the digital camera weights color channels.</span></span></p>
<p><span data-ttu-id="26979-363">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="26979-363">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="26979-364">以下是這個屬性的可能值清單。</span><span class="sxs-lookup"><span data-stu-id="26979-364">The following is a list of possible values for this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="26979-365">白色餘額</span><span class="sxs-lookup"><span data-stu-id="26979-365">White Balance</span></span></th>
<th><span data-ttu-id="26979-366">Description</span><span class="sxs-lookup"><span data-stu-id="26979-366">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26979-367">WHITEBALANCE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="26979-367">WHITEBALANCE_MANUAL</span></span></td>
<td><span data-ttu-id="26979-368">您可以使用 <strong>WIA_DPC_RGB_GAIN</strong> 屬性直接設定白色餘額。</span><span class="sxs-lookup"><span data-stu-id="26979-368">The white balance is set directly using the <strong>WIA_DPC_RGB_GAIN</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-369">WHITEBALANCE_AUTO</span><span class="sxs-lookup"><span data-stu-id="26979-369">WHITEBALANCE_AUTO</span></span></td>
<td><span data-ttu-id="26979-370">相機會使用自動機制來設定白色餘額。</span><span class="sxs-lookup"><span data-stu-id="26979-370">The camera uses an automatic mechanism to set the white balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-371">WHITEBALANCE_ONEPUSH_AUTO</span><span class="sxs-lookup"><span data-stu-id="26979-371">WHITEBALANCE_ONEPUSH_AUTO</span></span></td>
<td><span data-ttu-id="26979-372">當使用者在將攝影機指向白色表面時按下 [捕捉] 按鈕時，相機會決定白色餘額設定。</span><span class="sxs-lookup"><span data-stu-id="26979-372">The camera determines the white balance setting when a user presses the capture button while pointing the camera at a white surface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-373">WHITEBALANCE_DAYLIGHT</span><span class="sxs-lookup"><span data-stu-id="26979-373">WHITEBALANCE_DAYLIGHT</span></span></td>
<td><span data-ttu-id="26979-374">攝影機會將白色餘額設定為適合用於日光節約條件的值。</span><span class="sxs-lookup"><span data-stu-id="26979-374">The camera sets the white balance to a value appropriate for use in daylight conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-375">WHITEBALANCE_FLORESCENT</span><span class="sxs-lookup"><span data-stu-id="26979-375">WHITEBALANCE_FLORESCENT</span></span></td>
<td><span data-ttu-id="26979-376">攝影機會將白色餘額設定為適合搭配螢光燈來源使用的值。</span><span class="sxs-lookup"><span data-stu-id="26979-376">The camera sets the white balance to a value appropriate for use with a fluorescent light source.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26979-377">WHITEBALANCE_TUNGSTEN</span><span class="sxs-lookup"><span data-stu-id="26979-377">WHITEBALANCE_TUNGSTEN</span></span></td>
<td><span data-ttu-id="26979-378">攝影機會將白色餘額設定為適合搭配 tungsten 光源使用的值。</span><span class="sxs-lookup"><span data-stu-id="26979-378">The camera sets the white balance to a value appropriate for use with a tungsten light source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26979-379">WHITEBALANCE_FLASH</span><span class="sxs-lookup"><span data-stu-id="26979-379">WHITEBALANCE_FLASH</span></span></td>
<td><span data-ttu-id="26979-380">攝影機會將白色餘額設定為適合搭配電子 flash 使用的值。</span><span class="sxs-lookup"><span data-stu-id="26979-380">The camera sets the white balance to a value appropriate for use with an electronic flash.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <span data-ttu-id="26979-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-382">描述 URL。</span><span class="sxs-lookup"><span data-stu-id="26979-382">Describes a URL.</span></span> <span data-ttu-id="26979-383">此 proroperty 所描述的 URL，是從裝置取得影像或物件之後，可以將其上傳至，根據下列其中一個案例。</span><span class="sxs-lookup"><span data-stu-id="26979-383">The URL described by this proroperty is one that images or objects, after they are acquired from the device, can be uploaded to—according to one of the following scenarios.</span></span></p>
<ul>
<li><span data-ttu-id="26979-384">WIA 應用程式會讀取此屬性，並允許使用者自動將影像上傳至 URL。</span><span class="sxs-lookup"><span data-stu-id="26979-384">A WIA application reads this property and allows the user to automatically upload images to the URL.</span></span></li>
<li><span data-ttu-id="26979-385">應用程式會將 URL 和其他裝置 (kiosk 等) 使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="26979-385">An application sets the URL, and other devices (kiosks and so forth) use this property.</span></span></li>
</ul>
<p><span data-ttu-id="26979-386">Microsoft Windows 不會自行上傳影像。</span><span class="sxs-lookup"><span data-stu-id="26979-386">Microsoft Windows does not upload images by itself.</span></span></p>
<p><span data-ttu-id="26979-387">Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-387">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <span data-ttu-id="26979-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-389">擁有者的名稱 ( 是裝置目前的使用者) 。</span><span class="sxs-lookup"><span data-stu-id="26979-389">The name of the owner ( which is the current user) of the device.</span></span> <span data-ttu-id="26979-390">裝置會使用這個屬性，在其所捕捉的每個 EXIF 映射中填入演出者欄位。</span><span class="sxs-lookup"><span data-stu-id="26979-390">The device uses this property to populate the Artist field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="26979-391">Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-391">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <span data-ttu-id="26979-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span><span class="sxs-lookup"><span data-stu-id="26979-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="26979-393">著作權通知。</span><span class="sxs-lookup"><span data-stu-id="26979-393">The copyright notification.</span></span> <span data-ttu-id="26979-394">裝置會使用這個屬性，在其所捕捉的每個 EXIF 映射中填入著作權欄位。</span><span class="sxs-lookup"><span data-stu-id="26979-394">The device uses this property to populate the Copyright field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="26979-395">Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="26979-395">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="26979-396">規格需求</span><span class="sxs-lookup"><span data-stu-id="26979-396">Requirements</span></span>



| <span data-ttu-id="26979-397">需求</span><span class="sxs-lookup"><span data-stu-id="26979-397">Requirement</span></span> | <span data-ttu-id="26979-398">值</span><span class="sxs-lookup"><span data-stu-id="26979-398">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26979-399">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26979-399">Minimum supported client</span></span><br/> | <span data-ttu-id="26979-400">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26979-400">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="26979-401">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26979-401">Minimum supported server</span></span><br/> | <span data-ttu-id="26979-402">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26979-402">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="26979-403">標頭</span><span class="sxs-lookup"><span data-stu-id="26979-403">Header</span></span><br/>                   | <dl> <span data-ttu-id="26979-404"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="26979-404"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




