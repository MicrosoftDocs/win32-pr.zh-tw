---
description: 下列常數指定一組有效的 Windows 映像取得 (WIA) 掃描器專案屬性。
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: '掃描器 WIA 專案屬性常數 (Wiadef. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aa3b1cc4ae14a9460a24f652a9599035cacca2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971004"
---
# <a name="scanner-wia-item-property-constants"></a><span data-ttu-id="0aec7-103">掃描器 WIA 專案屬性常數</span><span class="sxs-lookup"><span data-stu-id="0aec7-103">Scanner WIA Item Property Constants</span></span>

<span data-ttu-id="0aec7-104">下列常數指定一組有效的 Windows 映像取得 (WIA) 掃描器專案屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-104">The following constants specify the valid set of Windows Image Acquisition (WIA) scanner item properties.</span></span>

<span data-ttu-id="0aec7-105">前置詞 "WIA \_ ip \_ " 表示掃描器裝置的專案屬性，而且是 C/c + + 中使用的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="0aec7-105">The prefix "WIA\_IPS\_" indicates an Item Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="0aec7-106">針對腳本用途，這些常數會使用前置詞 "ScannerPicture"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。</span><span class="sxs-lookup"><span data-stu-id="0aec7-106">For scripting purposes these constants use the prefix "ScannerPicture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="0aec7-107">來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。</span><span class="sxs-lookup"><span data-stu-id="0aec7-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0aec7-108">常數/值</span><span class="sxs-lookup"><span data-stu-id="0aec7-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0aec7-109">Description</span><span class="sxs-lookup"><span data-stu-id="0aec7-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <span data-ttu-id="0aec7-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-111">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-111">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="0aec7-112">開啟或關閉自動反扭曲。</span><span class="sxs-lookup"><span data-stu-id="0aec7-112">Turns automatic deskew on or off.</span></span><br/> <span data-ttu-id="0aec7-113">僅限 WIA_CATEGORY_FEEDER 的選擇性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-113">Optional for WIA_CATEGORY_FEEDER only.</span></span><br/> <span data-ttu-id="0aec7-114">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-114">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="0aec7-115">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-115">The following table has the constants that are valid with this property.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-116">常數</span><span class="sxs-lookup"><span data-stu-id="0aec7-116">Constant</span></span></th>
<th><span data-ttu-id="0aec7-117">描述</span><span class="sxs-lookup"><span data-stu-id="0aec7-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-118">WIA_AUTO_DESKEW_ON</span><span class="sxs-lookup"><span data-stu-id="0aec7-118">WIA_AUTO_DESKEW_ON</span></span></td>
<td><span data-ttu-id="0aec7-119">開啟自動反扭曲。</span><span class="sxs-lookup"><span data-stu-id="0aec7-119">Turn on automatic deskew.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-120">WIA_AUTO_DESKEW_OFF</span><span class="sxs-lookup"><span data-stu-id="0aec7-120">WIA_AUTO_DESKEW_OFF</span></span></td>
<td><span data-ttu-id="0aec7-121">關閉自動反扭曲。</span><span class="sxs-lookup"><span data-stu-id="0aec7-121">Turn off automatic deskew.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <span data-ttu-id="0aec7-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-123">掃描器內可用的影像亮度值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-123">The image brightness values available within the scanner.</span></span></p>
<p><span data-ttu-id="0aec7-124">包含裝置目前的硬體亮度設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-124">Contains the current hardware brightness setting for the device.</span></span> <span data-ttu-id="0aec7-125">應用程式會將此屬性設定為硬體的亮度值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-125">An application sets this property to the hardware's brightness value.</span></span> <span data-ttu-id="0aec7-126">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-126">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-127">值的對應範圍介於-1000 到1000之間，其中1000對應到最大亮度、0對應于標準亮度，而-1000 對應至最小亮度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-127">Values should be mapped in a range from -1000 through 1000, where 1000 corresponds to the maximum brightness, 0 corresponds to normal brightness, and -1000 corresponds to the minimum brightness.</span></span></p>
<p><span data-ttu-id="0aec7-128">類別中所有專案的必要專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-128">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="0aec7-129">選擇性，但建議用於支援預覽的 WIA_CATEGORY_FINISHED_FILE 專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-129">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="0aec7-130">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-130">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <span data-ttu-id="0aec7-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-132">包含裝置目前的硬體對比設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-132">Contains the current hardware contrast setting for a device.</span></span> <span data-ttu-id="0aec7-133">應用程式會將此屬性設定為硬體的對比值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-133">An application sets this property to the hardware's contrast value.</span></span> <span data-ttu-id="0aec7-134">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-134">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-135">值的對應範圍介於-1000 到1000之間，其中-1000 對應至最小對比度、0對應至正常對比，而1000對應到最大對比度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-135">Values should be mapped in a range from -1000 through 1000, where -1000 corresponds to the minimum contrast, 0 corresponds to normal contrast, and 1000 corresponds to the maximum contrast.</span></span></p>
<p><span data-ttu-id="0aec7-136">類別中所有專案的必要專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-136">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="0aec7-137">選擇性，但建議用於支援預覽的 WIA_CATEGORY_FINISHED_FILE 專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-137">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="0aec7-138">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-138">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <span data-ttu-id="0aec7-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-140">包含目前的意圖設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-140">Contains the current intent settings.</span></span> <span data-ttu-id="0aec7-141">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-141">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-142">所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-142">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="0aec7-143">WIA_CATEGORY_FINISHED_FILE 或 WIA_CATEGORY_FOLDER 專案不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="0aec7-143">It is not supported for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="0aec7-144">類型： <strong>VT_I4</strong> 存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-144">Type: <strong>VT_I4</strong> Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span></span></p>
<p><span data-ttu-id="0aec7-145">驅動程式會根據應用程式的預期用途，使用這些專案來設定專案屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-145">The driver uses these to preset item properties based on an application's intended use of the image.</span></span> <span data-ttu-id="0aec7-146">例如，這可能包括最高品質、最小大小等等。</span><span class="sxs-lookup"><span data-stu-id="0aec7-146">This might include, for example, maximum quality, minimum size, and so on.</span></span></p>
<p><span data-ttu-id="0aec7-147">驅動程式會選擇位深度（以英寸為單位），而其所決定的其他設定則適用于所選意圖。</span><span class="sxs-lookup"><span data-stu-id="0aec7-147">The driver chooses the bit depth, in dots per inch, and other settings that it determines are appropriate for the selected intent.</span></span> <span data-ttu-id="0aec7-148">應用程式會由應用程式讀取目前的設定，以判斷哪些屬性已變更。</span><span class="sxs-lookup"><span data-stu-id="0aec7-148">It is up to the application to read the current settings to determine which properties were changed.</span></span> <span data-ttu-id="0aec7-149">應用程式會設定此屬性，以自動設定特定取得意圖的 WIA 屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-149">An application sets this property to auto-set the WIA properties for specific acquisition intent.</span></span> <span data-ttu-id="0aec7-150">所有掃描器都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-150">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="0aec7-151">應用程式會設定此屬性，以自動設定特定取得意圖的 WIA 屬性</span><span class="sxs-lookup"><span data-stu-id="0aec7-151">An application sets this property to auto-set the WIA properties for specific acquisition intent</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-152">旗標可以與位 <strong>or</strong> 運算子結合，但影像不能同時為灰階和 color。</span><span class="sxs-lookup"><span data-stu-id="0aec7-152">The flags can be combined with a bitwise <strong>OR</strong> operator, but an image cannot be both grayscale and color.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-153">所有掃描器都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-153">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="0aec7-154">下表包含影像類型旗標及其定義。</span><span class="sxs-lookup"><span data-stu-id="0aec7-154">The following table contains the image-type flags and their definitions.</span></span> <span data-ttu-id="0aec7-155">這些旗標用來設定要使用的影像類型：色彩、灰階等等。</span><span class="sxs-lookup"><span data-stu-id="0aec7-155">These flags are used to set which type of image is intended: color, grayscale, and so on.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-156">預定的影像類型旗標</span><span class="sxs-lookup"><span data-stu-id="0aec7-156">Intended image type flags</span></span></th>
<th><span data-ttu-id="0aec7-157">Description</span><span class="sxs-lookup"><span data-stu-id="0aec7-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-158">WIA_INTENT_NONE</span><span class="sxs-lookup"><span data-stu-id="0aec7-158">WIA_INTENT_NONE</span></span></td>
<td><span data-ttu-id="0aec7-159">預設值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-159">Default value.</span></span> <span data-ttu-id="0aec7-160">未指定意圖。</span><span class="sxs-lookup"><span data-stu-id="0aec7-160">No intent is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-161">WIA_INTENT_IMAGE_TYPE_COLOR</span><span class="sxs-lookup"><span data-stu-id="0aec7-161">WIA_INTENT_IMAGE_TYPE_COLOR</span></span></td>
<td><span data-ttu-id="0aec7-162">應用程式打算將裝置準備好進行色彩掃描。</span><span class="sxs-lookup"><span data-stu-id="0aec7-162">The application intends to prepare the device for a color scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="0aec7-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span></span></td>
<td><span data-ttu-id="0aec7-164">應用程式打算將裝置準備好進行灰階掃描。</span><span class="sxs-lookup"><span data-stu-id="0aec7-164">The application intends to prepare the device for a grayscale scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-165">WIA_INTENT_IMAGE_TYPE_TEXT</span><span class="sxs-lookup"><span data-stu-id="0aec7-165">WIA_INTENT_IMAGE_TYPE_TEXT</span></span></td>
<td><span data-ttu-id="0aec7-166">應用程式打算準備裝置來掃描文字。</span><span class="sxs-lookup"><span data-stu-id="0aec7-166">The application intends to prepare the device for scanning text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-167">WIA_INTENT_IMAGE_TYPE_MASK</span><span class="sxs-lookup"><span data-stu-id="0aec7-167">WIA_INTENT_IMAGE_TYPE_MASK</span></span></td>
<td><span data-ttu-id="0aec7-168">所有影像類型旗標的遮罩。</span><span class="sxs-lookup"><span data-stu-id="0aec7-168">Mask for all of the image-type flags.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0aec7-169">下表包含品質和大小旗標及其定義。</span><span class="sxs-lookup"><span data-stu-id="0aec7-169">The following table contains the quality and size flags and their definitions.</span></span> <span data-ttu-id="0aec7-170">這些旗標是用來設定預期的品質等級。</span><span class="sxs-lookup"><span data-stu-id="0aec7-170">These flags are used to set which level of quality is intended.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-171">預定的影像大小/品質旗標</span><span class="sxs-lookup"><span data-stu-id="0aec7-171">Intended image size/quality flags</span></span></th>
<th><span data-ttu-id="0aec7-172">Description</span><span class="sxs-lookup"><span data-stu-id="0aec7-172">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-173">WIA_INTENT_MINIMIZE_SIZE</span><span class="sxs-lookup"><span data-stu-id="0aec7-173">WIA_INTENT_MINIMIZE_SIZE</span></span></td>
<td><span data-ttu-id="0aec7-174">應用程式會準備裝置來掃描產生的影像，以進行小型掃描。</span><span class="sxs-lookup"><span data-stu-id="0aec7-174">The application intends to prepare the device for scanning an image that result's in a small scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-175">WIA_INTENT_MAXIMIZE_QUALITY</span><span class="sxs-lookup"><span data-stu-id="0aec7-175">WIA_INTENT_MAXIMIZE_QUALITY</span></span></td>
<td><span data-ttu-id="0aec7-176">應用程式打算準備裝置來掃描高品質的影像。</span><span class="sxs-lookup"><span data-stu-id="0aec7-176">The application intends to prepare the device for scanning a high-quality image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-177">WIA_INTENT_SIZE_MASK</span><span class="sxs-lookup"><span data-stu-id="0aec7-177">WIA_INTENT_SIZE_MASK</span></span></td>
<td><span data-ttu-id="0aec7-178">此旗標是所有大小/品質旗標的遮罩。</span><span class="sxs-lookup"><span data-stu-id="0aec7-178">This flag is a mask for all of the size/quality flags.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-179">WIA_INTENT_BEST_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="0aec7-179">WIA_INTENT_BEST_PREVIEW</span></span></td>
<td><span data-ttu-id="0aec7-180">應用程式打算準備裝置以掃描預覽。</span><span class="sxs-lookup"><span data-stu-id="0aec7-180">The application intends to prepare the device for scanning a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <span data-ttu-id="0aec7-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-182">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-182">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-183">包含 x 方向的圖元數，從 WIA_IPS_XPOS 到要 deskewed 之影像最上方角落的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="0aec7-183">Contains the number of pixels in the x-direction from WIA_IPS_XPOS to the x-coordinate of the uppermost corner of the image to be deskewed.</span></span> <span data-ttu-id="0aec7-184">因此，它會結合 WIA_IPS_DESKEW_Y，其中扭曲影像的兩個頂角位於 WIA_IPS_XPOS、WIA_IPS_YPOS、WIA_IPS_XEXTENT 和 WIA_IPS_YEXTENT 所定義的周框中。</span><span class="sxs-lookup"><span data-stu-id="0aec7-184">Hence, it describes, in conjunction with WIA_IPS_DESKEW_Y, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="0aec7-185">如果支援 deskewing，則會由掃描器驅動程式來執行它的屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-185">his property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="0aec7-186">WIA_IPS_DESKEW_X 的有效值必須介於0到 (WIA_IPS_XEXTENT-1) 之間。</span><span class="sxs-lookup"><span data-stu-id="0aec7-186">The valid values for WIA_IPS_DESKEW_X must be between 0 and (WIA_IPS_XEXTENT - 1).</span></span> <span data-ttu-id="0aec7-187">0值表示不應該執行扭曲。</span><span class="sxs-lookup"><span data-stu-id="0aec7-187">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="0aec7-188">針對 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER 和 WIA_CATEGORY_FILM 類別目錄的專案，這個屬性是選擇性的。而且無法 WIA_CATEGORY_FINISHED_FILE 或 WIA_CATEGORY_FOLDER 專案使用。</span><span class="sxs-lookup"><span data-stu-id="0aec7-188">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="0aec7-189">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="0aec7-189">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <span data-ttu-id="0aec7-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-191">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-191">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-192">包含 y 方向的圖元數，從 WIA_IPS_YPOS 到要 deskewed 之影像最左邊角落的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="0aec7-192">Contains the number of pixels in the y-direction from WIA_IPS_YPOS to the y-coordinate of the leftmost corner of the image to be deskewed.</span></span> <span data-ttu-id="0aec7-193">因此，它會結合 WIA_IPS_DESKEW_X，其中扭曲影像的兩個頂角位於 WIA_IPS_XPOS、WIA_IPS_YPOS、WIA_IPS_XEXTENT 和 WIA_IPS_YEXTENT 所定義的周框中。</span><span class="sxs-lookup"><span data-stu-id="0aec7-193">Hence, it describes, in conjunction with WIA_IPS_DESKEW_X, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="0aec7-194">如果支援 deskewing，則會由掃描器驅動程式來執行這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-194">This property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="0aec7-195">WIA_IPS_DESKEW_Y 的有效值必須介於0到 (WIA_IPS_YEXTENT-1) 之間。</span><span class="sxs-lookup"><span data-stu-id="0aec7-195">The valid values for WIA_IPS_DESKEW_Y must be between 0 and (WIA_IPS_YEXTENT - 1).</span></span> <span data-ttu-id="0aec7-196">0值表示不應該執行扭曲。</span><span class="sxs-lookup"><span data-stu-id="0aec7-196">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="0aec7-197">針對 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER 和 WIA_CATEGORY_FILM 類別目錄的專案，這個屬性是選擇性的。而且無法 WIA_CATEGORY_FINISHED_FILE 或 WIA_CATEGORY_FOLDER 專案使用。</span><span class="sxs-lookup"><span data-stu-id="0aec7-197">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="0aec7-198">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="0aec7-198">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <span data-ttu-id="0aec7-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-200">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-200">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-201">包含目前的掃描器取得來源和模式。</span><span class="sxs-lookup"><span data-stu-id="0aec7-201">Contains the current scanner acquisition source and mode.</span></span> <span data-ttu-id="0aec7-202">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-202">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-203">應用程式會讀取此屬性，以判斷掃描器的目前取得來源，或撰寫此屬性來設定掃描器的來源和模式。</span><span class="sxs-lookup"><span data-stu-id="0aec7-203">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="0aec7-204">此外，應用程式也會使用此屬性來啟用和停用雙面列印程式功能。</span><span class="sxs-lookup"><span data-stu-id="0aec7-204">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="0aec7-205">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-205">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="0aec7-206">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-206">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-207">Flags</span><span class="sxs-lookup"><span data-stu-id="0aec7-207">Flags</span></span></th>
<th><span data-ttu-id="0aec7-208">Description</span><span class="sxs-lookup"><span data-stu-id="0aec7-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-209">雙工</span><span class="sxs-lookup"><span data-stu-id="0aec7-209">DUPLEX</span></span></td>
<td><span data-ttu-id="0aec7-210">使用雙面列印器作業掃描。</span><span class="sxs-lookup"><span data-stu-id="0aec7-210">Scan using duplexer operations.</span></span> <span data-ttu-id="0aec7-211">使用針對送紙器專案所設定的一般設定來掃描兩個檔側 (WIA_CATEGORY_FEEDER) 。</span><span class="sxs-lookup"><span data-stu-id="0aec7-211">Scan both document sides using common settings configured for the feeder item (WIA_CATEGORY_FEEDER).</span></span> <span data-ttu-id="0aec7-212">無法同時設定雙工和 ADVANCE_DUPLEX。</span><span class="sxs-lookup"><span data-stu-id="0aec7-212">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-213">ADVANCED_DUPLEX</span><span class="sxs-lookup"><span data-stu-id="0aec7-213">ADVANCED_DUPLEX</span></span></td>
<td><span data-ttu-id="0aec7-214">使用為每個子送紙器專案設定的個別設定進行掃描 (WIA_CATEGORY_FEEDER_FRONT 和 WIA_CATEGORY_FEEDER_BACK) 。</span><span class="sxs-lookup"><span data-stu-id="0aec7-214">Scan using individual settings configured for each child feeder item (WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK).</span></span> <span data-ttu-id="0aec7-215">無法同時設定雙工和 ADVANCE_DUPLEX。</span><span class="sxs-lookup"><span data-stu-id="0aec7-215">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-216">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="0aec7-216">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="0aec7-217">先掃描檔的前方。</span><span class="sxs-lookup"><span data-stu-id="0aec7-217">Scan the front of the document first.</span></span> <span data-ttu-id="0aec7-218">當設定了雙工或 ADVANCED_DUPLEX 時，此值有效。</span><span class="sxs-lookup"><span data-stu-id="0aec7-218">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-219">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="0aec7-219">BACK_FIRST</span></span></td>
<td><span data-ttu-id="0aec7-220">先掃描檔的背面。</span><span class="sxs-lookup"><span data-stu-id="0aec7-220">Scan the back of the document first.</span></span> <span data-ttu-id="0aec7-221">當設定了雙工或 ADVANCED_DUPLEX 時，此值有效。</span><span class="sxs-lookup"><span data-stu-id="0aec7-221">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-222">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="0aec7-222">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="0aec7-223">只掃描前方。</span><span class="sxs-lookup"><span data-stu-id="0aec7-223">Scan the front only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-224">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="0aec7-224">BACK_ONLY</span></span></td>
<td><span data-ttu-id="0aec7-225">只掃描回來。</span><span class="sxs-lookup"><span data-stu-id="0aec7-225">Scan the back only.</span></span> <span data-ttu-id="0aec7-226">當設定了雙工或 ADVANCED_DUPLEX 時，此值有效。</span><span class="sxs-lookup"><span data-stu-id="0aec7-226">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <span data-ttu-id="0aec7-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-228">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-228">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-229">當有一個以上的檔案時，可指定特定電影掃描附件的規格。</span><span class="sxs-lookup"><span data-stu-id="0aec7-229">Enables specification of a particular film scanning attachment when there is more than one.</span></span></p>
<p><span data-ttu-id="0aec7-230">當有多個膠捲掃描專案時，WIA_CATEGORY_FILM 專案需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-230">This property is required for the WIA_CATEGORY_FILM items when there are multiple film scan items.</span></span> <span data-ttu-id="0aec7-231">如果裝置只支援一個根掃描器膠捲專案，則此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0aec7-231">If the device supports only one root scanner film item then this property is optional.</span></span></p>
<p><span data-ttu-id="0aec7-232">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-232">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0aec7-233">允許的值： BSTR 的格式應為 @ResourceBinary ， <ResourceID> 以允許當地語系化，因為此字串會透過膠捲掃描 UI 向使用者公開。</span><span class="sxs-lookup"><span data-stu-id="0aec7-233">Allowed values: The BSTR should be in the form of @ResourceBinary,-<ResourceID> to allow localization as this string would be exposed to the user through the film scanning UI.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <span data-ttu-id="0aec7-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-235">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-235">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-236">啟用目前電影掃描的設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-236">Enables configuration of the current film scan.</span></span></p>
<p><span data-ttu-id="0aec7-237">WIA_CATEGORY_FILM 專案需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-237">This property is required for the WIA_CATEGORY_FILM item.</span></span></p>
<p><span data-ttu-id="0aec7-238">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-238">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0aec7-239">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-239">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-240">常數</span><span class="sxs-lookup"><span data-stu-id="0aec7-240">Constant</span></span></th>
<th><span data-ttu-id="0aec7-241">描述</span><span class="sxs-lookup"><span data-stu-id="0aec7-241">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-242">WIA_FILM_COLOR_SLIDE</span><span class="sxs-lookup"><span data-stu-id="0aec7-242">WIA_FILM_COLOR_SLIDE</span></span></td>
<td><span data-ttu-id="0aec7-243">掃描彩色投影片。</span><span class="sxs-lookup"><span data-stu-id="0aec7-243">Scan for a color slide.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-244">WIA_FILM_COLOR_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="0aec7-244">WIA_FILM_COLOR_NEGATIVE</span></span></td>
<td><span data-ttu-id="0aec7-245">掃描是否有負面的色彩。</span><span class="sxs-lookup"><span data-stu-id="0aec7-245">Scan for a color negative.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-246">WIA_FILM_BW_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="0aec7-246">WIA_FILM_BW_NEGATIVE</span></span></td>
<td><span data-ttu-id="0aec7-247">掃描黑色和白色的負面。</span><span class="sxs-lookup"><span data-stu-id="0aec7-247">Scan for a black and white negative.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <span data-ttu-id="0aec7-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-249">保留供未來使用，並不會在此時間執行。</span><span class="sxs-lookup"><span data-stu-id="0aec7-249">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="0aec7-250">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-250">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="0aec7-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-252">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-252">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-253">指定 WIA_CATEGORY_FOLDER 專案中儲存的專案數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-253">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="0aec7-254">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-254">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <span data-ttu-id="0aec7-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-256">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-256">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-257">開啟或關閉掃描器燈。</span><span class="sxs-lookup"><span data-stu-id="0aec7-257">Turns the scanner lamp on or off.</span></span></p>
<p><span data-ttu-id="0aec7-258">針對 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER 和 WIA_CATEGORY_FILM 專案為選擇性，並建議用於 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-258">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-259">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-259">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0aec7-260">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-260">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-261">常數</span><span class="sxs-lookup"><span data-stu-id="0aec7-261">Constant</span></span></th>
<th><span data-ttu-id="0aec7-262">描述</span><span class="sxs-lookup"><span data-stu-id="0aec7-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-263">WIA_LAMP_ON</span><span class="sxs-lookup"><span data-stu-id="0aec7-263">WIA_LAMP_ON</span></span></td>
<td><span data-ttu-id="0aec7-264">開啟燈泡。</span><span class="sxs-lookup"><span data-stu-id="0aec7-264">Turn on the lamp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-265">WIA_LAMP_OFF</span><span class="sxs-lookup"><span data-stu-id="0aec7-265">WIA_LAMP_OFF</span></span></td>
<td><span data-ttu-id="0aec7-266">關閉燈。</span><span class="sxs-lookup"><span data-stu-id="0aec7-266">Turn off the lamp.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <span data-ttu-id="0aec7-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-268">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-268">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-269">設定當掃描器未使用時，保持燈的最長時間。</span><span class="sxs-lookup"><span data-stu-id="0aec7-269">Sets the maximum time to keep the lamp on when the scanner is not being used.</span></span></p>
<p><span data-ttu-id="0aec7-270">針對 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER 和 WIA_CATEGORY_FILM 專案為選擇性，並建議用於 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-270">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-271">類型： <strong>VT_UI4</strong>、存取：讀取/寫入、有效的值： 0-0xFFF 秒</span><span class="sxs-lookup"><span data-stu-id="0aec7-271">Type: <strong>VT_UI4</strong>, Access: Read/Write, Valid Values: 0 - 0xFFF seconds</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <span data-ttu-id="0aec7-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-273">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-273">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-274">指定目前解析度的水準 (X) 軸中掃描的最大寬度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-274">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span> <span data-ttu-id="0aec7-275">這可能是工作表輸送或掃描床的寬度（根據專案類型）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-275">This may be the width of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="0aec7-276">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <span data-ttu-id="0aec7-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-278">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-278">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-279">指定目前解析度的垂直 (Y) 軸中掃描的最大高度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-279">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span> <span data-ttu-id="0aec7-280">這可能是工作表輸送或掃描床的高度（根據專案類型而定）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-280">This may be the height of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="0aec7-281">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-281">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <span data-ttu-id="0aec7-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-283">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-283">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-284">指定目前解析度的水準 (X) 軸掃描的最小寬度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-284">Specifies the minimum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="0aec7-285">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-285">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <span data-ttu-id="0aec7-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-287">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-287">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-288">指定目前解析度的垂直 (Y) 軸中掃描的最小高度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-288">Specifies the minimum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="0aec7-289">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-289">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <span data-ttu-id="0aec7-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-291">保留供未來使用，並不會在此時間執行。</span><span class="sxs-lookup"><span data-stu-id="0aec7-291">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="0aec7-292">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-292">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <span data-ttu-id="0aec7-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-294">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-294">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-295">水準光學解析度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-295">Horizontal Optical Resolution.</span></span> <span data-ttu-id="0aec7-296">最高支援的水準光學解析度（DPI）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-296">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="0aec7-297">這個屬性是單一值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-297">This property is a single value.</span></span> <span data-ttu-id="0aec7-298">這不是可由裝置產生的所有解決方案的清單。</span><span class="sxs-lookup"><span data-stu-id="0aec7-298">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="0aec7-299">相反地，這是裝置光纖的解析度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-299">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="0aec7-300">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-300">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="0aec7-301">所有專案都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-301">This property is required for all items.</span></span></p>
<p><span data-ttu-id="0aec7-302">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-302">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <span data-ttu-id="0aec7-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-304">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-304">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-305">垂直光學解析度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-305">Vertical Optical Resolution.</span></span> <span data-ttu-id="0aec7-306">支援的最高垂直光學解析度（DPI）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-306">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="0aec7-307">這個屬性是單一值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-307">This property is a single value.</span></span> <span data-ttu-id="0aec7-308">這不是裝置產生的所有解決方案的清單。</span><span class="sxs-lookup"><span data-stu-id="0aec7-308">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="0aec7-309">相反地，這是裝置光纖的解析度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-309">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="0aec7-310">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-310">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="0aec7-311">所有專案都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-311">This property is required for all items.</span></span></p>
<p><span data-ttu-id="0aec7-312">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <span data-ttu-id="0aec7-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-314">指定要掃描之檔的目前方向。</span><span class="sxs-lookup"><span data-stu-id="0aec7-314">Specifies the current orientation of the documents to be scanned.</span></span> <span data-ttu-id="0aec7-315">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-315">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-316">應用程式會設定此屬性，以定義要取得之頁面或影像的原始方向。</span><span class="sxs-lookup"><span data-stu-id="0aec7-316">An application sets this property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="0aec7-317">如需如何使用 WIA_IPS_ORIENTATION 的詳細資訊，請參閱 <strong>WIA_IPS_PAGE_SIZE</strong>。</span><span class="sxs-lookup"><span data-stu-id="0aec7-317">For information on how to use WIA_IPS_ORIENTATION, see <strong>WIA_IPS_PAGE_SIZE</strong>.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-318">WIA_IPS_ORIENTATION 指的是要在掃描器床或輸送器上掃描的檔位置。</span><span class="sxs-lookup"><span data-stu-id="0aec7-318">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="0aec7-319">這是相對於掃描方向的檔方向。</span><span class="sxs-lookup"><span data-stu-id="0aec7-319">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="0aec7-320">WIA_IPS_ROTATION 指的是在影像傳送至應用程式之前，在掃描影像之後套用的旋轉。</span><span class="sxs-lookup"><span data-stu-id="0aec7-320">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-321">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-321">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0aec7-322">下表包含四個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-322">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-323">值</span><span class="sxs-lookup"><span data-stu-id="0aec7-323">Value</span></span></th>
<th><span data-ttu-id="0aec7-324">定義</span><span class="sxs-lookup"><span data-stu-id="0aec7-324">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-325">肖像</span><span class="sxs-lookup"><span data-stu-id="0aec7-325">PORTRAIT</span></span></td>
<td><span data-ttu-id="0aec7-326">0度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-326">0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-327">景觀</span><span class="sxs-lookup"><span data-stu-id="0aec7-327">LANDSCAPE</span></span></td>
<td><span data-ttu-id="0aec7-328">相對於直向的順向計數器旋轉旋轉。90</span><span class="sxs-lookup"><span data-stu-id="0aec7-328">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-329">ROT180</span><span class="sxs-lookup"><span data-stu-id="0aec7-329">ROT180</span></span></td>
<td><span data-ttu-id="0aec7-330">相對於直向的順向計數器旋轉旋轉。180</span><span class="sxs-lookup"><span data-stu-id="0aec7-330">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-331">ROT270</span><span class="sxs-lookup"><span data-stu-id="0aec7-331">ROT270</span></span></td>
<td><span data-ttu-id="0aec7-332">相對於直向的順向計數器旋轉旋轉。270</span><span class="sxs-lookup"><span data-stu-id="0aec7-332">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <span data-ttu-id="0aec7-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-334">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-334">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-335">包含目前已設定要掃描的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="0aec7-335">Contains the size of the page that is currently set to be scanned.</span></span> <span data-ttu-id="0aec7-336">應用程式會設定此屬性，以選取要掃描的頁面維度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-336">An application sets this property to select the dimensions of the page to scan.</span></span> <span data-ttu-id="0aec7-337">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-337">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-338">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-338">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0aec7-339">如需可搭配這個屬性使用的常數，請參閱 <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2.0 頁面大小常數</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="0aec7-339">For the constants that can be used with this property, see <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2.0 Page Size Constants</strong></a>.</span></span> <span data-ttu-id="0aec7-340">請注意這些非固定大小，特別是：</span><span class="sxs-lookup"><span data-stu-id="0aec7-340">Note these non-fixed sizes, in particular:</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-341">值</span><span class="sxs-lookup"><span data-stu-id="0aec7-341">Value</span></span></th>
<th><span data-ttu-id="0aec7-342">定義</span><span class="sxs-lookup"><span data-stu-id="0aec7-342">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-343">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="0aec7-343">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="0aec7-344">由 <strong>WIA_IPS_PAGE_HEIGHT</strong> 的值和 <strong>WIA_IPS_PAGE_WIDTH</strong> 屬性定義。</span><span class="sxs-lookup"><span data-stu-id="0aec7-344">Defined by the values of the <strong>WIA_IPS_PAGE_HEIGHT</strong> and <strong>WIA_IPS_PAGE_WIDTH</strong> properties.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-345">WIA_PAGE_AUTO</span><span class="sxs-lookup"><span data-stu-id="0aec7-345">WIA_PAGE_AUTO</span></span></td>
<td><span data-ttu-id="0aec7-346">裝置會自動決定頁面大小。</span><span class="sxs-lookup"><span data-stu-id="0aec7-346">Page size is automatically determined by the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-347">WIA_PAGE_CUSTOM_BASE</span><span class="sxs-lookup"><span data-stu-id="0aec7-347">WIA_PAGE_CUSTOM_BASE</span></span></td>
<td><span data-ttu-id="0aec7-348">應用程式和設備磁碟機已經知道其維度的自訂頁面大小。</span><span class="sxs-lookup"><span data-stu-id="0aec7-348">A custom page size whose dimensions are already known to the application and the device driver.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0aec7-349"><strong>WIA_IPS_ORIENTATION</strong>屬性的值會決定目前選取之頁面的方向。</span><span class="sxs-lookup"><span data-stu-id="0aec7-349">The value of the <strong>WIA_IPS_ORIENTATION</strong> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="0aec7-350"><strong>WIA_IPS_PAGE_WIDTH</strong>和<strong>WIA_IPS_PAGE_HEIGHT</strong>屬性會報告頁面的尺寸（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-350">The <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="0aec7-351">這些屬性必須與 <strong>WIA_IPS_XEXTENT</strong> 和 <strong>WIA_IPS_YEXTENT</strong>一致，其中包含頁面的尺寸（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-351">These properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-352">WIA_PROP_LIST 類型的有效值取決於 <strong>WIA_IPS_ORIENTATION</strong> 屬性的有效設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-352">Valid values of type WIA_PROP_LIST depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="0aec7-353">例如，如果裝置無法使用 WIA_PAGE_A4 設定來掃描橫向導向的檔，當<strong>WIA_IPS_ORIENTATION</strong>設定為 [橫向] 時，WIA_PAGE_A4 不是<strong>WIA_IPS_PAGE_SIZE</strong>屬性的有效值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-353">If, for example, the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 is not a valid value for the <strong>WIA_IPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-354">如果應用程式將 <strong>WIA_IPS_PAGE_SIZE</strong> 設定為上表中的三個以外的任何值，則迷你驅動程式應該將 <strong>WIA_IPS_PAGE_WIDTH</strong> 的值和 <strong>WIA_IPS_PAGE_HEIGHT</strong> 調整為頁面的尺寸（以英寸為萬分之一）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-354">If an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to any value other than the three in the table above, the minidriver should adjust the values of <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="0aec7-355">它也應該調整 <strong>WIA_IPS_XEXTENT</strong> 的值，並 <strong>WIA_IPS_YEXTENT</strong> 為頁面的尺寸（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-355">It should also adjust the values of <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="0aec7-356">如果範圍設定 (<strong>WIA_IPS_XEXTENT</strong> 或 <strong>WIA_IPS_YEXTENT</strong>) 變更為不符合目前 [頁面大小] 設定的值，則迷你驅動程式應該將 [ <strong>WIA_IPS_PAGE_SIZE</strong> ] 屬性的值變更為 [WIA_PAGE_CUSTOM]。</span><span class="sxs-lookup"><span data-stu-id="0aec7-356">If an extent setting (<strong>WIA_IPS_XEXTENT</strong> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page size setting, the minidriver should change the value of the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="0aec7-357">迷你驅動程式也應該根據新的範圍設定來修改 <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> 或 <strong>WIA_IPS_PAGE_HEIGHT</strong> 。</span><span class="sxs-lookup"><span data-stu-id="0aec7-357">The minidriver should also modify <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> or <strong>WIA_IPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="0aec7-358">如果 <strong>WIA_IPS_ORIENTATION</strong> 設定為 [橫向]，則會相對於其一般值來交換範圍設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-358">If <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE, the extent settings will be exchanged relative to their usual values.</span></span> <span data-ttu-id="0aec7-359">例如，如果應用程式將 <strong>WIA_IPS_PAGE_SIZE</strong> 設定為 WIA_PAGE_A4，迷你驅動程式會將 <strong>WIA_IPS_PAGE_WIDTH</strong> 設定為11692，並將 <strong>WIA_IPS_PAGE_HEIGHT</strong> 設定為8267。</span><span class="sxs-lookup"><span data-stu-id="0aec7-359">For example, if an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver sets <strong>WIA_IPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_IPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="0aec7-360"> (迷你驅動程式也應據以調整 <strong>WIA_IPS_XEXTENT</strong> 和 <strong>WIA_IPS_YEXTENT</strong> 。 ) </span><span class="sxs-lookup"><span data-stu-id="0aec7-360">(The minidriver should also adjust <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.)</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-361">如果 <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> 設為 WIA_PAGE_CUSTOM，則不會使用方向設定來決定要掃描之頁面的範圍維度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-361">If <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-362">迷你驅動程式負責確保 <strong>WIA_IPS_ORIENTATION</strong> 屬性與目前的選取區域一致。</span><span class="sxs-lookup"><span data-stu-id="0aec7-362">The minidriver is responsible for ensuring that the <strong>WIA_IPS_ORIENTATION</strong> property is in agreement with the current selection area.</span></span> <span data-ttu-id="0aec7-363">如果應用程式將 <strong>WIA_IPS_ORIENTATION</strong> 的值變更為目前選取之頁面大小不正確值，則迷你驅動程式應該將 <strong>WIA_IPS_PAGE_SIZE</strong> 的值變更為新的方向值所支援的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="0aec7-363">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_IPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="0aec7-364">如果應用程式將 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM，則目前的選取範圍不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="0aec7-364">If an application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="0aec7-365">WIA 迷你驅動程式應該會從目前的 <strong>WIA_IPS_XPOS</strong> 設定開始，取得目前的影像版面配置，並 <strong>WIA_IPS_YPOS</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-365">The WIA minidriver should obtain the current image layout, starting from the current settings of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="0aec7-366">如果 [頁面大小] 設定產生的選取區域位於掃描器的床之外，則迷你驅動程式必須自動調整 <strong>WIA_IPS_XPOS</strong> 的值，並 <strong>WIA_IPS_YPOS</strong> 屬性設定為有效的設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-366">If the page size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="0aec7-367">如果 <strong>WIA_IPS_PAGE_SIZE</strong> 和 <strong>WIA_IPS_ORIENTATION</strong> 屬性同時設定，且在組合套用時無效，則迷你驅動程式應該會在 <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv：:d rvvalidateitemproperties</a>中傳回錯誤，以使應用程式的設定失敗。</span><span class="sxs-lookup"><span data-stu-id="0aec7-367">If the <strong>WIA_IPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span></p>
<p><span data-ttu-id="0aec7-368">下列四個範例顯示不同 <strong>WIA_IPS_PAGE_SIZE</strong> 案例。</span><span class="sxs-lookup"><span data-stu-id="0aec7-368">The following four examples show different <strong>WIA_IPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="0aec7-369">驅動程式會報告設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-369">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="0aec7-370">應用程式會將 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_LETTER。</span><span class="sxs-lookup"><span data-stu-id="0aec7-370">An application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="0aec7-371">應用程式會將 <strong>WIA_IPS_ORIENTATION</strong> 屬性設定為橫向。</span><span class="sxs-lookup"><span data-stu-id="0aec7-371">An application sets the <strong>WIA_IPS_ORIENTATION</strong> property to LANDSCAPE.</span></span></li>
<li><span data-ttu-id="0aec7-372">應用程式會將 <strong>WIA_IPS_XEXTENT</strong> 屬性變更為較小的值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-372">An application changes the <strong>WIA_IPS_XEXTENT</strong> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="0aec7-373"><strong>範例1：迷你驅動程式報告設定</strong></span><span class="sxs-lookup"><span data-stu-id="0aec7-373"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="0aec7-374">在下列範例中，迷你驅動程式會在應用程式設定任何 WIA 屬性之前，設定自訂選取區域。</span><span class="sxs-lookup"><span data-stu-id="0aec7-374">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="0aec7-375">在此情況下，選取區域代表整個平板。</span><span class="sxs-lookup"><span data-stu-id="0aec7-375">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="0aec7-376"><strong>範例2：應用程式將</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>屬性設定為 WIA_PAGE_LETTER</strong></span><span class="sxs-lookup"><span data-stu-id="0aec7-376"><strong>Example 2: An application sets the</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="0aec7-377"><strong>範例3：應用程式將</strong> <strong>WIA_IPS_ORIENTATION</strong>  <strong>屬性設定為橫向</strong></span><span class="sxs-lookup"><span data-stu-id="0aec7-377"><strong>Example 3: An application sets the</strong> <strong>WIA_IPS_ORIENTATION</strong>  <strong>property to LANDSCAPE</strong></span></span></p>
<p><span data-ttu-id="0aec7-378">實體床必須能夠取得原本處於橫向方向的頁面。</span><span class="sxs-lookup"><span data-stu-id="0aec7-378">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="0aec7-379"><strong>範例4：應用程式</strong>將 <strong>WIA_IPS_XEXTENT</strong> <strong>屬性變更為較小的值</strong></span><span class="sxs-lookup"><span data-stu-id="0aec7-379"><strong>Example 4: An application changes the</strong> <strong>WIA_IPS_XEXTENT</strong> <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="0aec7-380">在下列範例中，應用程式會將 <strong>WIA_IPS_XEXTENT</strong> 屬性變更為1000。</span><span class="sxs-lookup"><span data-stu-id="0aec7-380">In the following example, an application changes the <strong>WIA_IPS_XEXTENT</strong> property to 1000.</span></span> <span data-ttu-id="0aec7-381">迷你驅動程式應該假設 <strong>WIA_IPS_XEXTENT</strong> 中包含的新值不再適用于 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性，因此應該將 <strong>WIA_IPS_PAGE_SIZE</strong> 變更為 WIA_PAGE_CUSTOM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-381">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_IPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="0aec7-382">迷你驅動程式也必須調整 <strong>WIA_IPS_PAGE_WIDTH</strong>。</span><span class="sxs-lookup"><span data-stu-id="0aec7-382">The minidriver must also adjust <strong>WIA_IPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <span data-ttu-id="0aec7-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-384">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-384">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-385">包含目前所選頁面的高度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-385">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="0aec7-386">迷你驅動程式會建立並維護 <strong>WIA_IPS_PAGE_HEIGHT</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-386">The minidriver creates and maintains the <strong>WIA_IPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="0aec7-387">應用程式會讀取此屬性，以判斷所掃描之頁面的實體維度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-387">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="0aec7-388">如果範圍設定與已知的頁面大小不同，這個屬性會報告頁面的高度，其 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM (這是 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性) 的值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-388">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_IPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="0aec7-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> 必須與 <strong>WIA_IPS_XEXTENT</strong>同步，以報告要掃描之頁面的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> must be in sync with <strong>WIA_IPS_XEXTENT</strong>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="0aec7-390">WIA_CATEGORY_FEEDER 專案需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-390">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="0aec7-391">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <span data-ttu-id="0aec7-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-393">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-393">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-394">包含目前所選取頁面的寬度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-394">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="0aec7-395">應用程式會讀取此屬性，以判斷所掃描之頁面的實體維度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-395">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="0aec7-396">如果範圍設定與已知的頁面大小不同，這個屬性會報告頁面的寬度，其 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-396">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="0aec7-397"><strong>WIA_IPS_PAGE_WIDTH</strong> 必須與 <strong>WIA_IPS_XEXTENT</strong>的值同步，這會報告要掃描頁面的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-397"><strong>WIA_IPS_PAGE_WIDTH</strong> must be in sync with the value of <strong>WIA_IPS_XEXTENT</strong>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="0aec7-398">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-398">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-399">WIA_CATEGORY_FEEDER 專案需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-399">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="0aec7-400">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-400">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <span data-ttu-id="0aec7-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-402">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-402">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-403">包含要從自動檔送紙器取得的目前頁面數目。</span><span class="sxs-lookup"><span data-stu-id="0aec7-403">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="0aec7-404">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-404">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-405">類型： <strong>VT_I4</strong>;存取：讀取/寫入;有效值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 此值為零，表示掃描器可掃描的最大頁數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-405">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> This is zero through the maximum number of pages that the scanner can scan.</span></span> <span data-ttu-id="0aec7-406">如果掃描器可以連續掃描，則此值為 ALL_PAGES (= 0) 。</span><span class="sxs-lookup"><span data-stu-id="0aec7-406">The value is ALL_PAGES (= 0) if the scanner can scan continuously.</span></span></p>
<p><span data-ttu-id="0aec7-407">應用程式會讀取此屬性，以判斷檔送紙器的頁面容量。</span><span class="sxs-lookup"><span data-stu-id="0aec7-407">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="0aec7-408">應用程式也會將此屬性設定為要掃描的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="0aec7-408">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-409">如果已啟用雙工模式 (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> 設定為 [送紙器] |雙工 |ADVANCED_DUPLEX) ， <strong>WIA_IPS_PAGES</strong> 仍等於要掃描的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="0aec7-409">If duplex mode is enabled (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-410">如果已啟用雙工，則會自動包含兩頁的紙張，即使頁面的後端是空白的。</span><span class="sxs-lookup"><span data-stu-id="0aec7-410">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="0aec7-411">將 <strong>WIA_IPS_PAGES</strong> 設定為1，會導致掃描器處理頁面的一側。</span><span class="sxs-lookup"><span data-stu-id="0aec7-411">Setting <strong>WIA_IPS_PAGES</strong> to 1 causes a scanner to process one side of the page.</span></span> <span data-ttu-id="0aec7-412">如果掃描器無法在雙工模式下掃描頁面的一端，則建議您將 WIA_PROPERTY_INFO 結構之範圍成員的 Inc 成員 <strong>WIA_IPS_PAGES</strong> 值變更為2。</span><span class="sxs-lookup"><span data-stu-id="0aec7-412">We recommend that, if a scanner is unable to scan only one side of a page while in duplex mode, you change the <strong>WIA_IPS_PAGES</strong> value for the Inc member of the Range member of the WIA_PROPERTY_INFO structure to 2.</span></span> <span data-ttu-id="0aec7-413">此值會通知應用程式，它必須以兩個的倍數要求頁面。</span><span class="sxs-lookup"><span data-stu-id="0aec7-413">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="0aec7-414">值為 ALL_PAGES (= 0) 表示要掃描目前載入檔送紙器中的 <em>所有</em> 頁面。</span><span class="sxs-lookup"><span data-stu-id="0aec7-414">A value of ALL_PAGES (= 0) means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <span data-ttu-id="0aec7-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-416">包含白色和黑色圖元的目前設定。</span><span class="sxs-lookup"><span data-stu-id="0aec7-416">Contains the current setting for white and black pixels.</span></span> <span data-ttu-id="0aec7-417">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-417">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-418">應用程式會讀取此值，以根據應用程式的執行) 來判斷白色或黑色 (的值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-418">An application reads this value to determine the value of WHITE or BLACK (depending on what the application is doing).</span></span></p>
<p><span data-ttu-id="0aec7-419">所有已啟用或已儲存的專案都需要。也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-419">Required for all acquisition enabled or stored items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="0aec7-420">WIA_CATEGORY_FOLDER 專案不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="0aec7-420">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="0aec7-421">類型： <strong>VT_I4</strong>;存取：讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>。</span><span class="sxs-lookup"><span data-stu-id="0aec7-421">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="0aec7-422">如果裝置只能設定為單一值，請建立 WIA_PROP_LIST 類型，並在其中放置有效的值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-422">If the device can be set to only a single value, create a WIA_PROP_LIST type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="0aec7-423">下表有兩個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-423">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-424">值</span><span class="sxs-lookup"><span data-stu-id="0aec7-424">Value</span></span></th>
<th><span data-ttu-id="0aec7-425">定義</span><span class="sxs-lookup"><span data-stu-id="0aec7-425">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-426">WIA_PHOTO_WHITE_0</span><span class="sxs-lookup"><span data-stu-id="0aec7-426">WIA_PHOTO_WHITE_0</span></span></td>
<td><span data-ttu-id="0aec7-427">白色為0，黑色為1。</span><span class="sxs-lookup"><span data-stu-id="0aec7-427">WHITE is 0, and BLACK is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-428">WIA_PHOTO_WHITE_1</span><span class="sxs-lookup"><span data-stu-id="0aec7-428">WIA_PHOTO_WHITE_1</span></span></td>
<td><span data-ttu-id="0aec7-429">白色為1，黑色為0。</span><span class="sxs-lookup"><span data-stu-id="0aec7-429">WHITE is 1, and BLACK is 0.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <span data-ttu-id="0aec7-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-431">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-431">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-432">指出裝置的預覽模式。</span><span class="sxs-lookup"><span data-stu-id="0aec7-432">Indicates the preview mode for a device.</span></span> <span data-ttu-id="0aec7-433">應用程式會設定此屬性，以將裝置置於預覽模式。</span><span class="sxs-lookup"><span data-stu-id="0aec7-433">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="0aec7-434">WIA_CATEGORY_FLATBED 和 WIA_CATEGORY_FILM 專案都需要這個屬性，WIA_CATEGORY_FEEDER 專案的選擇性專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-434">This property is required for the WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items, optional for the WIA_CATEGORY_FEEDER item.</span></span></p>
<p><span data-ttu-id="0aec7-435">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-435">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0aec7-436">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-436">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-437">值</span><span class="sxs-lookup"><span data-stu-id="0aec7-437">Value</span></span></th>
<th><span data-ttu-id="0aec7-438">定義</span><span class="sxs-lookup"><span data-stu-id="0aec7-438">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-439">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="0aec7-439">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="0aec7-440">應用程式將會執行最後的掃描。</span><span class="sxs-lookup"><span data-stu-id="0aec7-440">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-441">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="0aec7-441">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="0aec7-442">應用程式將會執行預覽掃描。</span><span class="sxs-lookup"><span data-stu-id="0aec7-442">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <span data-ttu-id="0aec7-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-444">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-444">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-445">指定是否可以在影像預覽期間更新現有的預覽影像， (以回應 WIA_IPA_DATATYPE 的變更或 WIA_IPA_DEPTH 屬性) 。</span><span class="sxs-lookup"><span data-stu-id="0aec7-445">Specifies whether the existing preview image can be updated during an image preview (in response to a change in the WIA_IPA_DATATYPE or WIA_IPA_DEPTH properties).</span></span></p>
<p><span data-ttu-id="0aec7-446">對於支援預覽掃描的所有啟用的專案，這個屬性是選擇性的。也就是說，WIA_PREVIEW_SCAN 支援 WIA_IPS_PREVIEW。</span><span class="sxs-lookup"><span data-stu-id="0aec7-446">This property is optional for all acquisition enabled items that support preview scans; that is, WIA_IPS_PREVIEW is supported with WIA_PREVIEW_SCAN.</span></span> <span data-ttu-id="0aec7-447">這包括類型 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM 的專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-447">This includes items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-448">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-448">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0aec7-449">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-449">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-450">常數</span><span class="sxs-lookup"><span data-stu-id="0aec7-450">Constant</span></span></th>
<th><span data-ttu-id="0aec7-451">描述</span><span class="sxs-lookup"><span data-stu-id="0aec7-451">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-452">WIA_ADVANCED_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="0aec7-452">WIA_ADVANCED_PREVIEW</span></span></td>
<td><span data-ttu-id="0aec7-453">您可以更新現有的映射。</span><span class="sxs-lookup"><span data-stu-id="0aec7-453">Updating the existing image is possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-454">WIA_BASIC_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="0aec7-454">WIA_BASIC_PREVIEW</span></span></td>
<td><span data-ttu-id="0aec7-455">必須執行另一個預覽掃描，因為無法更新現有的映射。</span><span class="sxs-lookup"><span data-stu-id="0aec7-455">Another preview scan must be executed because updating the existing image is not possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <span data-ttu-id="0aec7-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-457">包含目前的旋轉設定（如果已執行）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-457">Contains the current rotation setting, if it is implemented.</span></span> <span data-ttu-id="0aec7-458">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-458">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-459">應用程式會設定此屬性，以通知驅動程式 (如果所有) 在驅動程式將映射傳回給應用程式之前，都要旋轉映射。</span><span class="sxs-lookup"><span data-stu-id="0aec7-459">An application sets this property to inform the driver how much (if at all) to rotate the image before the driver returns it to the application.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-460">WIA_IPS_ORIENTATION 指的是要在掃描器床或輸送器上掃描的檔位置。</span><span class="sxs-lookup"><span data-stu-id="0aec7-460">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="0aec7-461">這是相對於掃描方向的檔方向。</span><span class="sxs-lookup"><span data-stu-id="0aec7-461">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="0aec7-462">WIA_IPS_ROTATION 指的是在影像傳送至應用程式之前，在掃描影像之後套用的旋轉。</span><span class="sxs-lookup"><span data-stu-id="0aec7-462">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-463">WIA 迷你驅動程式會負責輪替影像資料，然後再將其傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="0aec7-463">The WIA minidriver is responsible for rotating the image data before sending it back to the application.</span></span> <span data-ttu-id="0aec7-464">應用程式會負責檢查影像標頭，以查看新旋轉的值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-464">The application is responsible for checking the image headers to see the newly rotated values.</span></span></p>
<p><span data-ttu-id="0aec7-465">解決目前影像選取區域的旋轉效果 (（由 <strong>WIA_IPS_XPOS</strong>、 <strong>WIA_IPS_YPOS</strong>、 <strong>WIA_IPS_XEXTENT</strong> 和 <strong>WIA_IPS_YEXTENT</strong> 屬性) 所定義）有相當大的混淆。</span><span class="sxs-lookup"><span data-stu-id="0aec7-465">Considerable confusion exists about resolving the effect of rotation on the current image's selection area (which is defined by the <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> properties).</span></span></p>
<p><span data-ttu-id="0aec7-466"><em>選取區域</em> 指的是實體掃描器床上要從中取得影像的選取區域。</span><span class="sxs-lookup"><span data-stu-id="0aec7-466"><em>Selection area</em> refers to the selected area on the physical scanner bed that an image is be acquired from.</span></span> <span data-ttu-id="0aec7-467"><strong>WIA_IPS_ROTATION</strong> 不會修改選取區域。</span><span class="sxs-lookup"><span data-stu-id="0aec7-467"><strong>WIA_IPS_ROTATION</strong> does not modify the selection area.</span></span> <span data-ttu-id="0aec7-468">只有在驅動程式取得適當的選取區域之後，驅動程式才會根據 <strong>WIA_IPS_ROTATION</strong> 來套用逆時針旋轉。</span><span class="sxs-lookup"><span data-stu-id="0aec7-468">The driver applies a counterclockwise rotation according to <strong>WIA_IPS_ROTATION</strong> only after the driver has acquired the appropriate selection area.</span></span> <span data-ttu-id="0aec7-469"><strong>WIA_IPS_ROTATION</strong> 會影響輸出影像的維度，因此這些維度必須反映在產生的影像資料標頭中。</span><span class="sxs-lookup"><span data-stu-id="0aec7-469"><strong>WIA_IPS_ROTATION</strong> does affect the dimensions of the output image, so these dimensions must be reflected in the resulting image's data header.</span></span></p>
<p><span data-ttu-id="0aec7-470">所有已啟用的專案都是選擇性的;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-470">Optional for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-471">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-471">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="0aec7-472">已定義下列旋轉常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-472">The following rotation constants are defined.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-473">常數</span><span class="sxs-lookup"><span data-stu-id="0aec7-473">Constant</span></span></th>
<th><span data-ttu-id="0aec7-474">定義</span><span class="sxs-lookup"><span data-stu-id="0aec7-474">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-475">肖像</span><span class="sxs-lookup"><span data-stu-id="0aec7-475">PORTRAIT</span></span></td>
<td><span data-ttu-id="0aec7-476">驅動程式將不會旋轉映射。</span><span class="sxs-lookup"><span data-stu-id="0aec7-476">The driver will not rotate the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-477">景觀</span><span class="sxs-lookup"><span data-stu-id="0aec7-477">LANDSCAPE</span></span></td>
<td><span data-ttu-id="0aec7-478">驅動程式會逆時針旋轉影像90度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-478">TThe driver rotates the image 90 degrees counterclockwise.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-479">ROT180</span><span class="sxs-lookup"><span data-stu-id="0aec7-479">ROT180</span></span></td>
<td><span data-ttu-id="0aec7-480">驅動程式會逆時針旋轉影像180度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-480">The driver rotates the image 180 degrees counterclockwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-481">ROT270</span><span class="sxs-lookup"><span data-stu-id="0aec7-481">ROT270</span></span></td>
<td><span data-ttu-id="0aec7-482">驅動程式會逆時針旋轉影像270度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-482">The driver rotates the image 270 degrees counterclockwise.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <span data-ttu-id="0aec7-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-484">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-484">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-485">指定應用程式是否應該使用驅動程式的分割篩選進行多重區域掃描。</span><span class="sxs-lookup"><span data-stu-id="0aec7-485">Specifies whether the application should use the driver's segmentation filter for multi-region scanning.</span></span> <span data-ttu-id="0aec7-486">如果 WIA_CATEGORY_FLATBED 和 WIA_CATEGORY_FILM 專案支援使用分割篩選來建立子專案，或是驅動程式本身為固定框架建立子專案，則必須為這些專案執行 WIA_IPS_SEGMENTATION。</span><span class="sxs-lookup"><span data-stu-id="0aec7-486">WIA_IPS_SEGMENTATION must be implemented for WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items if they support either the creation of child items with a segmentation filter or if the driver itself creates child items for fixed frames.</span></span></p>
<p><span data-ttu-id="0aec7-487">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-487">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0aec7-488">下表有兩個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-488">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-489">值</span><span class="sxs-lookup"><span data-stu-id="0aec7-489">Value</span></span></th>
<th><span data-ttu-id="0aec7-490">定義</span><span class="sxs-lookup"><span data-stu-id="0aec7-490">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-491">WIA_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="0aec7-491">WIA_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="0aec7-492">應用程式應該使用分割篩選進行多重區域掃描。</span><span class="sxs-lookup"><span data-stu-id="0aec7-492">The application should use the segmentation filter for multi-region scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-493">WIA_DONT_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="0aec7-493">WIA_DONT_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="0aec7-494">驅動程式會針對多重區域掃描建立子專案本身。</span><span class="sxs-lookup"><span data-stu-id="0aec7-494">The driver creates the child items itself for multi-region scanning.</span></span> <span data-ttu-id="0aec7-495">如果掃描器針對此用途使用固定的框架，通常會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0aec7-495">This is usually the case if the scanner uses fixed frames for this purpose.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-496">驅動程式可能會隨附分割篩選，但仍有 WIA_IPS_SEGMENTATION 設定為其中一個專案的 WIA_DONT_USE_SEGMENTATION_FILTER (例如 WIA_CATEGORY_FILM 專案) 。</span><span class="sxs-lookup"><span data-stu-id="0aec7-496">It is possible for a driver to come with a segmentation filter, but still have WIA_IPS_SEGMENTATION set to WIA_DONT_USE_SEGMENTATION_FILTER for one of its items (such as, the WIA_CATEGORY_FILM item).</span></span> <span data-ttu-id="0aec7-497">如果掃描器使用固定的框架進行膠片掃描，但無法從 WIA_CATEGORY_FLATBED 專案進行一般掃描，就可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0aec7-497">This could be the case if the scanner uses fixed frames for film scanning, but not for regular scanning from WIA_CATEGORY_FLATBED items.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <span data-ttu-id="0aec7-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-499">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-499">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-500">包含放置於平板之檔的註冊（或對齊和邊緣偵測）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-500">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="0aec7-501">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-501">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="0aec7-502">這個屬性會指出工作表如何水準定位於掌上型或紙匣掃描器的掃描標頭上。</span><span class="sxs-lookup"><span data-stu-id="0aec7-502">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="0aec7-503">屬性是用來預測檔放置於掃描標頭的哪個位置。</span><span class="sxs-lookup"><span data-stu-id="0aec7-503">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="0aec7-504">如果掃描器支援一個以上的掃描標頭，這個屬性會相對於最上層的掃描標頭。</span><span class="sxs-lookup"><span data-stu-id="0aec7-504">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="0aec7-505">這是工作表、捲軸和掌上型掃描器的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-505">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="0aec7-506">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-506">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0aec7-507">下表有三個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-507">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-508">常數</span><span class="sxs-lookup"><span data-stu-id="0aec7-508">Constant</span></span></th>
<th><span data-ttu-id="0aec7-509">描述</span><span class="sxs-lookup"><span data-stu-id="0aec7-509">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-510">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="0aec7-510">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="0aec7-511">工作表在掃描標頭的相對位置。</span><span class="sxs-lookup"><span data-stu-id="0aec7-511">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-512">中心</span><span class="sxs-lookup"><span data-stu-id="0aec7-512">CENTERED</span></span></td>
<td><span data-ttu-id="0aec7-513">工作表會以掃描標頭為中心。</span><span class="sxs-lookup"><span data-stu-id="0aec7-513">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0aec7-514">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="0aec7-514">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="0aec7-515">工作表位於掃描標頭的右邊。</span><span class="sxs-lookup"><span data-stu-id="0aec7-515">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <span data-ttu-id="0aec7-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-517">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-517">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-518">指出專案是否需要向使用者顯示預覽控制項。</span><span class="sxs-lookup"><span data-stu-id="0aec7-518">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="0aec7-519">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-519">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-520">所有已啟用傳輸的專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="0aec7-520">Optional for all transfer enabled items.</span></span> <span data-ttu-id="0aec7-521">這通常只是類別目錄的專案 WIA_ITEM_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FILM 和 WIA_CATEGORY_FINISHED_FILE。</span><span class="sxs-lookup"><span data-stu-id="0aec7-521">This is usually just items of the categories WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM, and WIA_CATEGORY_FINISHED_FILE.</span></span></p>
<p><span data-ttu-id="0aec7-522">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-522">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="0aec7-523">下表包含對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="0aec7-523">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0aec7-524">常數</span><span class="sxs-lookup"><span data-stu-id="0aec7-524">Constant</span></span></th>
<th><span data-ttu-id="0aec7-525">描述</span><span class="sxs-lookup"><span data-stu-id="0aec7-525">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0aec7-526">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="0aec7-526">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="0aec7-527">顯示使用者的預覽控制項，因為此裝置可以執行預覽。</span><span class="sxs-lookup"><span data-stu-id="0aec7-527">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0aec7-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="0aec7-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="0aec7-529">不要向使用者顯示預覽控制項，因為此裝置無法執行預覽。</span><span class="sxs-lookup"><span data-stu-id="0aec7-529">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <span data-ttu-id="0aec7-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-531">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-531">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-532">指定應用程式 (或篩選) 是否可以在目前專案下建立子專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-532">Specifies whether the application (or the filters) can create child items under the current item.</span></span></p>
<p><span data-ttu-id="0aec7-533">所有已啟用傳輸專案類別的選擇性： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FILM 甚至 WIA_CATEGORY_FOLDER。</span><span class="sxs-lookup"><span data-stu-id="0aec7-533">Optional for all transfer enabled item categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM and even WIA_CATEGORY_FOLDER.</span></span> <span data-ttu-id="0aec7-534"> (如果儲存體不支援上傳新的專案，則此屬性應該是不支援或不支援的 <strong>FALSE</strong> 值。 ) </span><span class="sxs-lookup"><span data-stu-id="0aec7-534">(If the storage won't support upload of new items then this property should be either unsupported or supported with the <strong>FALSE</strong> value.)</span></span></p>
<p><span data-ttu-id="0aec7-535">支援 WIA_IPS_SEGMENTATION 和 WIA_USE_SEGMENTATION_FILTER 的專案也必須支援 WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION，並將其設定為 <strong>TRUE</strong>。</span><span class="sxs-lookup"><span data-stu-id="0aec7-535">Items supporting WIA_IPS_SEGMENTATION and WIA_USE_SEGMENTATION_FILTER must also support WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION and have it set to <strong>TRUE</strong>.</span></span></p>
<p><span data-ttu-id="0aec7-536">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <strong>TRUE</strong> 和 <strong>FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="0aec7-536">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <strong>TRUE</strong> and <strong>FALSE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <span data-ttu-id="0aec7-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-538">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-538">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-539">指定當影像轉換為單色時，可判斷圖元是否會轉換成白色或黑色的灰階值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-539">Specifies the grayscale value that determines whether a pixel will be converted to white or black when an image is converted to monochromatic.</span></span> <span data-ttu-id="0aec7-540">超過閾值的圖元變成白色。</span><span class="sxs-lookup"><span data-stu-id="0aec7-540">Pixels above the threshold become white.</span></span> <span data-ttu-id="0aec7-541">低於閾值的圖元變成白色。</span><span class="sxs-lookup"><span data-stu-id="0aec7-541">Pixels below the threshold become white.</span></span></p>
<p><span data-ttu-id="0aec7-542">支援 1 bpp 掃描且將 WIA_IPA_DATATYPE 屬性設定為 WIA_DATA_THRESHOLD 的取得專案，需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-542">This property is required for acquisition items that support 1-bpp scans and that have the WIA_IPA_DATATYPE property set to WIA_DATA_THRESHOLD.</span></span></p>
<p><span data-ttu-id="0aec7-543">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-543">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <span data-ttu-id="0aec7-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-545">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-545">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-546">指定驅動程式是否能夠在單一傳送呼叫中傳送多個子專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-546">Specifies whether the driver is capable of transferring multiple child items in single transfer call.</span></span></p>
<p><span data-ttu-id="0aec7-547">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-547">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="0aec7-548">這個屬性的唯一可能值是 WIA_TRANSFER_CHILDREN_SINGLE_SCAN。</span><span class="sxs-lookup"><span data-stu-id="0aec7-548">The only possible value for this property is WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span></span> <span data-ttu-id="0aec7-549">如果設定此旗標，則驅動程式能夠在單一傳送呼叫中傳輸多個子專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-549">If this flag is set, then the driver is capable of transfering multiple child items in single transfer call.</span></span> <span data-ttu-id="0aec7-550">如果未設定旗標，則 WIA 服務會以遞迴方式逐一查看子專案，然後傳送每一個專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-550">If the flag is not set, the WIA Service will walk through the child items recursively and then transfer each of those items.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="0aec7-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-552">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-552">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-553">指定要為專案上傳的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0aec7-553">Specifies the number of bytes to upload for the item.</span></span></p>
<p><span data-ttu-id="0aec7-554">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-554">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <span data-ttu-id="0aec7-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-556">在開始掃描工作之前，指定裝置所需的最大準備時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-556">Specifies the maximum warm-up time, in milliseconds, that the device needs before starting the scanning operation.</span></span> <span data-ttu-id="0aec7-557">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-557">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-558">應用程式可以讀取此屬性，以判斷此裝置的最大準備時間。</span><span class="sxs-lookup"><span data-stu-id="0aec7-558">An application can read this property to determine the maximum warm-up time for this device.</span></span> <span data-ttu-id="0aec7-559">然後，它會顯示 &quot; [正在等待裝置準備 &quot; ] 對話方塊，讓使用者知道等待或暫停可能會在發生任何情況之前發生。</span><span class="sxs-lookup"><span data-stu-id="0aec7-559">It can then present a &quot;waiting for the device to warm up&quot; dialog box, to let the user know that a wait or pause might occur before anything happens.</span></span></p>
<p><span data-ttu-id="0aec7-560">所有取得的已啟用專案都需要這個屬性;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-560">This property is required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-561">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <span data-ttu-id="0aec7-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-563">包含要取得之所選影像的目前寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-563">Contains the current width, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="0aec7-564">應用程式會設定這個屬性，將選取區域的寬度標示為取得。</span><span class="sxs-lookup"><span data-stu-id="0aec7-564">An application sets this property to mark the width of a selection area to acquire.</span></span> <span data-ttu-id="0aec7-565">這個屬性必須與 <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> 屬性一致。</span><span class="sxs-lookup"><span data-stu-id="0aec7-565">This property must agree with the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="0aec7-566">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-566">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-567">所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-567">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-568">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-568">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <span data-ttu-id="0aec7-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-570">包含所選影像左上角的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-570">Contains the x coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="0aec7-571">應用程式會將這個屬性設定為標示選取區域的左上角。</span><span class="sxs-lookup"><span data-stu-id="0aec7-571">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="0aec7-572">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-572">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-573">所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-573">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="0aec7-574">WIA_CATEGORY_FOLDER 專案不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="0aec7-574">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="0aec7-575">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-575">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <span data-ttu-id="0aec7-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-577">包含裝置目前的水準解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-577">Contains the current horizontal resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="0aec7-578">應用程式會設定這個屬性來設定水準解析度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-578">An application sets this property to set the horizontal resolution.</span></span> <span data-ttu-id="0aec7-579">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-579">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-580">如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-580">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="0aec7-581">這也是一個解決方式設定相依于另一個解決方法的情況。</span><span class="sxs-lookup"><span data-stu-id="0aec7-581">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="0aec7-582"> (垂直解析度可能取決於水準解析度。 ) </span><span class="sxs-lookup"><span data-stu-id="0aec7-582">(The vertical resolution can depend on the horizontal resolution.)</span></span></p>
<p><span data-ttu-id="0aec7-583">所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-583">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="0aec7-584">WIA_CATEGORY_FOLDER 專案不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="0aec7-584">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="0aec7-585">類型： <strong>VT_I4</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 或 WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="0aec7-585">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <span data-ttu-id="0aec7-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-587">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-587">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-588">設定可套用至掃描器裝置或其驅動程式內掃描影像的水準縮放（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-588">Sets the horizontal scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="0aec7-589">針對所有已啟用的專案，這個屬性是選擇性的;也就是說，WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM 類型的專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-589">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-590">類型： <strong>VT_I4</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE。</span><span class="sxs-lookup"><span data-stu-id="0aec7-590">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="0aec7-591">值可以是1到最大 VT_I4 (0xFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="0aec7-591">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="0aec7-592">例如，100表示無縮放比例，050表示相應減少為原始大小的50%，而200表示相應減少為原始大小的200%。</span><span class="sxs-lookup"><span data-stu-id="0aec7-592">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <span data-ttu-id="0aec7-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-594">包含要取得之所選影像的目前高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-594">Contains the current height, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="0aec7-595">應用程式會將這個屬性設定為標示選取區域的高度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-595">An application sets this property to mark the height of a selection area.</span></span> <span data-ttu-id="0aec7-596">這個屬性必須與 <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> 屬性的值一致。</span><span class="sxs-lookup"><span data-stu-id="0aec7-596">This property must be agree with the value of the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="0aec7-597">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-597">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-598">所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-598">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-599">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-599">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <span data-ttu-id="0aec7-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-601">所選影像左上角的目前 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-601">Current y coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="0aec7-602">應用程式會將這個屬性設定為標示選取區域的左上角。</span><span class="sxs-lookup"><span data-stu-id="0aec7-602">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="0aec7-603">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-603">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-604">所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-604">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="0aec7-605">WIA_CATEGORY_FOLDER 專案不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="0aec7-605">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="0aec7-606">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="0aec7-606">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <span data-ttu-id="0aec7-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="0aec7-608">包含裝置目前的垂直解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-608">Contains the current vertical resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="0aec7-609">應用程式會設定這個屬性來設定垂直解析度。</span><span class="sxs-lookup"><span data-stu-id="0aec7-609">An application sets this property to set the vertical resolution.</span></span> <span data-ttu-id="0aec7-610">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-610">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="0aec7-611">如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。</span><span class="sxs-lookup"><span data-stu-id="0aec7-611">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="0aec7-612">這也是一個解決方式設定相依于另一個解決方法的情況。</span><span class="sxs-lookup"><span data-stu-id="0aec7-612">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="0aec7-613"> (水準解析度可能取決於垂直解析度。 ) </span><span class="sxs-lookup"><span data-stu-id="0aec7-613">(The horizontal resolution can depend on the vertical resolution.)</span></span></p>
<p><span data-ttu-id="0aec7-614">所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。</span><span class="sxs-lookup"><span data-stu-id="0aec7-614">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="0aec7-615">WIA_CATEGORY_FOLDER 專案不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="0aec7-615">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="0aec7-616">類型： <strong>VT_I4</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 或 WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="0aec7-616">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <span data-ttu-id="0aec7-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="0aec7-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="0aec7-618">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0aec7-618">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="0aec7-619">設定可套用至掃描器裝置或其驅動程式內掃描影像的垂直縮放比例（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="0aec7-619">Sets the vertical scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="0aec7-620">針對所有已啟用的專案，這個屬性是選擇性的;也就是說，WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM 類型的專案。</span><span class="sxs-lookup"><span data-stu-id="0aec7-620">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="0aec7-621">類型： <strong>VT_I4</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE。</span><span class="sxs-lookup"><span data-stu-id="0aec7-621">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="0aec7-622">值可以是1到最大 VT_I4 (0xFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="0aec7-622">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="0aec7-623">例如，100表示無縮放比例，050表示相應減少為原始大小的50%，而200表示相應減少為原始大小的200%。</span><span class="sxs-lookup"><span data-stu-id="0aec7-623">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="0aec7-624">規格需求</span><span class="sxs-lookup"><span data-stu-id="0aec7-624">Requirements</span></span>



| <span data-ttu-id="0aec7-625">需求</span><span class="sxs-lookup"><span data-stu-id="0aec7-625">Requirement</span></span> | <span data-ttu-id="0aec7-626">值</span><span class="sxs-lookup"><span data-stu-id="0aec7-626">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0aec7-627">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0aec7-627">Minimum supported client</span></span><br/> | <span data-ttu-id="0aec7-628">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0aec7-628">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0aec7-629">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0aec7-629">Minimum supported server</span></span><br/> | <span data-ttu-id="0aec7-630">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0aec7-630">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0aec7-631">標頭</span><span class="sxs-lookup"><span data-stu-id="0aec7-631">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aec7-632"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="0aec7-632"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




