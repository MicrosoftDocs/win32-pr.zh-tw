---
description: Windows 映像取得 (WIA) 硬體裝置具有儲存在 Windows 登錄中的屬性值。
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: '掃描器裝置屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971005"
---
# <a name="scanner-device-property-constants"></a><span data-ttu-id="37a0e-103">掃描器裝置屬性常數</span><span class="sxs-lookup"><span data-stu-id="37a0e-103">Scanner Device Property Constants</span></span>

<span data-ttu-id="37a0e-104">Windows 映像取得 (WIA) 硬體裝置具有儲存在 Windows 登錄中的屬性值。</span><span class="sxs-lookup"><span data-stu-id="37a0e-104">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="37a0e-105">如需詳細資訊，請參閱 [**一般裝置屬性常數**](-wia-wiaitempropcommondevice.md)。</span><span class="sxs-lookup"><span data-stu-id="37a0e-105">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span> <span data-ttu-id="37a0e-106">下列裝置屬性常數（與其相關聯的字串）是數位影像掃描器的特定常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-106">The following device property constants, with their associated strings, are specific to digital image scanners.</span></span>

<span data-ttu-id="37a0e-107">前置詞 "WIA \_ DPS \_ " 表示掃描器裝置的裝置屬性，而且是 C/c + + 中使用的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="37a0e-107">The prefix "WIA\_DPS\_" indicates a Device Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="37a0e-108">針對腳本用途，這些常數會使用前置詞 "ScannerDevice"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。</span><span class="sxs-lookup"><span data-stu-id="37a0e-108">For scripting purposes these constants use the prefix "ScannerDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="37a0e-109">來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。</span><span class="sxs-lookup"><span data-stu-id="37a0e-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="37a0e-110">常數/值</span><span class="sxs-lookup"><span data-stu-id="37a0e-110">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="37a0e-111">Description</span><span class="sxs-lookup"><span data-stu-id="37a0e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <span data-ttu-id="37a0e-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-113">只有在 Windows Vista 和更新版本上才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-113">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="37a0e-114">包含 web 服務掃描器裝置的唯一函數實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="37a0e-114">Contains a unique function instance identifier for a web services scanner device.</span></span> <span data-ttu-id="37a0e-115">此識別碼代表 WIA 迷你驅動程式用來進行通訊的掃描器裝置上的 web 服務。</span><span class="sxs-lookup"><span data-stu-id="37a0e-115">This identifier represents the web service on the scanner device with which the WIA mini-driver is communicating.</span></span> <span data-ttu-id="37a0e-116">這項識別碼的表單不應進行任何假設。</span><span class="sxs-lookup"><span data-stu-id="37a0e-116">No assumptions about the form of this identifier should be made.</span></span> <span data-ttu-id="37a0e-117">WIA 迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-117">The WIA mini-driver creates and maintains this property.</span></span> <br/> <span data-ttu-id="37a0e-118">WIA 應用程式可使用「函式探索 API」這項 WIA_DPS_DEVICE_ID 的值，來尋找目前 WIA 2.0 會話中使用的 web 服務掃描器裝置的函式實例物件。</span><span class="sxs-lookup"><span data-stu-id="37a0e-118">WIA applications can use the value of WIA_DPS_DEVICE_ID to find, using the Function Discovery API, the function instance object representing the web services scanner device used in the current WIA 2.0 session.</span></span><br/> <span data-ttu-id="37a0e-119">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-119">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <span data-ttu-id="37a0e-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="37a0e-121">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="37a0e-121">Reserved, do not use.</span></span><br/> <span data-ttu-id="37a0e-122">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-122">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <span data-ttu-id="37a0e-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="37a0e-124">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="37a0e-124">Reserved, do not use.</span></span><br/> <span data-ttu-id="37a0e-125">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-125">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <span data-ttu-id="37a0e-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="37a0e-127">包含掃描器的功能。</span><span class="sxs-lookup"><span data-stu-id="37a0e-127">Contains the capabilities of the scanner.</span></span> <span data-ttu-id="37a0e-128">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-128">The minidriver creates and maintains this property.</span></span> <br/> <span data-ttu-id="37a0e-129">應用程式會讀取此屬性，以判斷掃描器是否已安裝平板、檔輸送器或雙面列印器。</span><span class="sxs-lookup"><span data-stu-id="37a0e-129">An application reads this property to determine whether the scanner has a flatbed, document feeder, or duplexer installed.</span></span> <span data-ttu-id="37a0e-130">這個屬性也可用來進一步定義已安裝的功能。</span><span class="sxs-lookup"><span data-stu-id="37a0e-130">This property is also used to further define the installed features.</span></span><br/> <span data-ttu-id="37a0e-131">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-131">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="37a0e-132">下表說明僅適用于 Windows 7 的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-132">The following table describes the constants that are valid with Windows 7 only.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-133">Flags</span><span class="sxs-lookup"><span data-stu-id="37a0e-133">Flags</span></span></th>
<th><span data-ttu-id="37a0e-134">Description</span><span class="sxs-lookup"><span data-stu-id="37a0e-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-135">AUTO_SOURCE</span><span class="sxs-lookup"><span data-stu-id="37a0e-135">AUTO_SOURCE</span></span></td>
<td><span data-ttu-id="37a0e-136">掃描器已安裝自動檔處理常式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-136">The scanner has an automatic document handler installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="37a0e-137">下表說明僅適用于 Windows 7 和 Windows Vista 的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-137">The following table describes the constants that are valid with Windows 7 and Windows Vista only.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-138">Flags</span><span class="sxs-lookup"><span data-stu-id="37a0e-138">Flags</span></span></th>
<th><span data-ttu-id="37a0e-139">Description</span><span class="sxs-lookup"><span data-stu-id="37a0e-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-140">ADVANCED_DUP</span><span class="sxs-lookup"><span data-stu-id="37a0e-140">ADVANCED_DUP</span></span></td>
<td><span data-ttu-id="37a0e-141">裝置支援 advanced 雙工掃描設定。</span><span class="sxs-lookup"><span data-stu-id="37a0e-141">The device supports advanced duplex scan configuration.</span></span> <span data-ttu-id="37a0e-142">使用 WIA_IPS_DUPLEX_SETTINGS 在使用基本和先進雙工設定之間切換。</span><span class="sxs-lookup"><span data-stu-id="37a0e-142">Use WIA_IPS_DUPLEX_SETTINGS to switch between using basic and advanced duplex configurations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-143">DETECT_FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="37a0e-143">DETECT_FILM_TPA</span></span></td>
<td><span data-ttu-id="37a0e-144">掃描器可以偵測透明/膠捲介面卡何時可以進行掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-144">The scanner can detect when the transparency/film adapter is ready to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-145">DETECT_STOR</span><span class="sxs-lookup"><span data-stu-id="37a0e-145">DETECT_STOR</span></span></td>
<td><span data-ttu-id="37a0e-146">掃描器可以偵測到內部儲存體中有檔時。</span><span class="sxs-lookup"><span data-stu-id="37a0e-146">The scanner can detect when there are documents in the internal storage.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-147">FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="37a0e-147">FILM_TPA</span></span></td>
<td><span data-ttu-id="37a0e-148">掃描器配備了透明/膠捲掃描介面卡。</span><span class="sxs-lookup"><span data-stu-id="37a0e-148">The scanner is equipped with a transparency/film scanning adapter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-149">STOR</span><span class="sxs-lookup"><span data-stu-id="37a0e-149">STOR</span></span></td>
<td><span data-ttu-id="37a0e-150">掃描器配備了內部影像儲存裝置。</span><span class="sxs-lookup"><span data-stu-id="37a0e-150">The scanner is equipped with an internal image storage device.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="37a0e-151">下表描述的是 Windows XP 或更新版本中有效的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-151">The following table describes the constants that are valid with Windows XP or later.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-152">Flags</span><span class="sxs-lookup"><span data-stu-id="37a0e-152">Flags</span></span></th>
<th><span data-ttu-id="37a0e-153">Description</span><span class="sxs-lookup"><span data-stu-id="37a0e-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-154">DETECT_FEED</span><span class="sxs-lookup"><span data-stu-id="37a0e-154">DETECT_FEED</span></span></td>
<td><span data-ttu-id="37a0e-155">掃描器可以偵測到送紙器中的檔。</span><span class="sxs-lookup"><span data-stu-id="37a0e-155">The scanner can detect a document in the feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-156">DETECT_FLAT</span><span class="sxs-lookup"><span data-stu-id="37a0e-156">DETECT_FLAT</span></span></td>
<td><span data-ttu-id="37a0e-157">掃描器可以偵測到平板玻璃上的檔。</span><span class="sxs-lookup"><span data-stu-id="37a0e-157">The scanner can detect a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-158">DETECT_SCAN</span><span class="sxs-lookup"><span data-stu-id="37a0e-158">DETECT_SCAN</span></span></td>
<td><span data-ttu-id="37a0e-159">掃描器只能透過掃描來偵測送紙器中的檔。</span><span class="sxs-lookup"><span data-stu-id="37a0e-159">The scanner can detect a document in the feeder only by scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-160">多重</span><span class="sxs-lookup"><span data-stu-id="37a0e-160">DUP</span></span></td>
<td><span data-ttu-id="37a0e-161">掃描器有雙面列印器。</span><span class="sxs-lookup"><span data-stu-id="37a0e-161">The scanner has a duplexer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-162">飼料</span><span class="sxs-lookup"><span data-stu-id="37a0e-162">FEED</span></span></td>
<td><span data-ttu-id="37a0e-163">掃描器已安裝自動檔處理常式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-163">The scanner has an automatic document handler installed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-164">平</span><span class="sxs-lookup"><span data-stu-id="37a0e-164">FLAT</span></span></td>
<td><span data-ttu-id="37a0e-165">掃描器有平板玻璃。</span><span class="sxs-lookup"><span data-stu-id="37a0e-165">The scanner has a flatbed platen.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="37a0e-166">下表說明僅適用于 Windows XP 的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-166">The following table describes the constants that are valid with Windows XP only.</span></span> <span data-ttu-id="37a0e-167">這些值在 Windows 7 和 Windows Vista 中已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="37a0e-167">These values have been deprecated for Windows 7 and Windows Vista and should not be used.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-168">Flags</span><span class="sxs-lookup"><span data-stu-id="37a0e-168">Flags</span></span></th>
<th><span data-ttu-id="37a0e-169">Description</span><span class="sxs-lookup"><span data-stu-id="37a0e-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-170">DETECT_DUP</span><span class="sxs-lookup"><span data-stu-id="37a0e-170">DETECT_DUP</span></span></td>
<td><span data-ttu-id="37a0e-171">掃描器可以偵測到使用者的雙工掃描要求。</span><span class="sxs-lookup"><span data-stu-id="37a0e-171">The scanner can detect a duplex scan request from the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-172">DETECT_DUP_AVAIL</span><span class="sxs-lookup"><span data-stu-id="37a0e-172">DETECT_DUP_AVAIL</span></span></td>
<td><span data-ttu-id="37a0e-173">掃描器可以分辨是否已安裝雙面列印程式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-173">The scanner can tell when the duplexer is installed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-174">DETECT_FEED_AVAIL</span><span class="sxs-lookup"><span data-stu-id="37a0e-174">DETECT_FEED_AVAIL</span></span></td>
<td><span data-ttu-id="37a0e-175">掃描器可以分辨自動檔送紙器的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="37a0e-175">The scanner can tell when the automatic document feeder is installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <span data-ttu-id="37a0e-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-177">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-177">This property is not supported in Windows Vista and later.</span></span> <span data-ttu-id="37a0e-178">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-179">包含目前的掃描器取得來源和模式。迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-179">Contains the current scanner acquisition source and mode.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-180">應用程式會讀取此屬性，以判斷掃描器的目前取得來源，或撰寫此屬性來設定掃描器的來源和模式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-180">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="37a0e-181">此外，應用程式也會使用此屬性來啟用和停用雙面列印程式功能。</span><span class="sxs-lookup"><span data-stu-id="37a0e-181">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="37a0e-182">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-182">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="37a0e-183">下表包含以這個屬性為有效的十個常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-183">The following table has the ten constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-184">Flags</span><span class="sxs-lookup"><span data-stu-id="37a0e-184">Flags</span></span></th>
<th><span data-ttu-id="37a0e-185">Description</span><span class="sxs-lookup"><span data-stu-id="37a0e-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-186">饋線</span><span class="sxs-lookup"><span data-stu-id="37a0e-186">FEEDER</span></span></td>
<td><span data-ttu-id="37a0e-187">使用檔送紙器進行掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-187">Scan using the document feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-188">平板</span><span class="sxs-lookup"><span data-stu-id="37a0e-188">FLATBED</span></span></td>
<td><span data-ttu-id="37a0e-189">使用平板的掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-189">Scan using the flatbed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-190">雙工</span><span class="sxs-lookup"><span data-stu-id="37a0e-190">DUPLEX</span></span></td>
<td><span data-ttu-id="37a0e-191">使用雙面列印器作業掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-191">Scan using duplexer operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-192">AUTO_ADVANCE</span><span class="sxs-lookup"><span data-stu-id="37a0e-192">AUTO_ADVANCE</span></span></td>
<td><span data-ttu-id="37a0e-193">在掃描之後啟用下一份檔的自動饋送。</span><span class="sxs-lookup"><span data-stu-id="37a0e-193">Enables automatic feeding of the next document after a scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-194">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="37a0e-194">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="37a0e-195">先掃描檔的前方。</span><span class="sxs-lookup"><span data-stu-id="37a0e-195">Scan the front of the document first.</span></span> <span data-ttu-id="37a0e-196">當設定雙工時，此值有效。</span><span class="sxs-lookup"><span data-stu-id="37a0e-196">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-197">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="37a0e-197">BACK_FIRST</span></span></td>
<td><span data-ttu-id="37a0e-198">先掃描檔的背面。</span><span class="sxs-lookup"><span data-stu-id="37a0e-198">Scan the back of the document first.</span></span> <span data-ttu-id="37a0e-199">當設定雙工時，此值有效。</span><span class="sxs-lookup"><span data-stu-id="37a0e-199">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-200">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="37a0e-200">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="37a0e-201">只掃描前方。</span><span class="sxs-lookup"><span data-stu-id="37a0e-201">Scan the front only.</span></span> <span data-ttu-id="37a0e-202">當設定雙工時，此值有效。</span><span class="sxs-lookup"><span data-stu-id="37a0e-202">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-203">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="37a0e-203">BACK_ONLY</span></span></td>
<td><span data-ttu-id="37a0e-204">只掃描回來。</span><span class="sxs-lookup"><span data-stu-id="37a0e-204">Scan the back only.</span></span> <span data-ttu-id="37a0e-205">當設定雙工時，此值有效。</span><span class="sxs-lookup"><span data-stu-id="37a0e-205">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-206">NEXT_PAGE</span><span class="sxs-lookup"><span data-stu-id="37a0e-206">NEXT_PAGE</span></span></td>
<td><span data-ttu-id="37a0e-207">掃描檔的下一頁。</span><span class="sxs-lookup"><span data-stu-id="37a0e-207">Scan the next page of the document.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-208">PREFEED</span><span class="sxs-lookup"><span data-stu-id="37a0e-208">PREFEED</span></span></td>
<td><span data-ttu-id="37a0e-209">啟用進紙前模式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-209">Enable pre-feed mode.</span></span> <span data-ttu-id="37a0e-210">掃描時預先定位下一個檔。</span><span class="sxs-lookup"><span data-stu-id="37a0e-210">Pre-position next document while scanning.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <span data-ttu-id="37a0e-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-212">包含掃描器安裝的平板、檔輸送器或雙面列印器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="37a0e-212">Contains current state of the scanner's installed flatbed, document feeder, or duplexer.</span></span> <span data-ttu-id="37a0e-213">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-213">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-214">應用程式會讀取此屬性，以判斷掃描器裝置是否已準備好可供使用。</span><span class="sxs-lookup"><span data-stu-id="37a0e-214">An application reads this property to determine whether the scanner device is ready to be used.</span></span> <span data-ttu-id="37a0e-215">在取得影像之前，這是檢查紙紙是否在紙器中的理想方式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-215">This is an ideal way to check whether paper is in the feeder prior to acquiring an image.</span></span></p>
<p><span data-ttu-id="37a0e-216">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-216">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-217">下表包含對此屬性有效的常數。星號 \* 表示 Windows Vista 或更新版本中不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="37a0e-217">The following table has the constants that are valid with this property.An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="37a0e-218"><strong>V</strong>符號表示只有在 Windows Vista 和更新版本中才支援旗標。</span><span class="sxs-lookup"><span data-stu-id="37a0e-218">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-219">Flags</span><span class="sxs-lookup"><span data-stu-id="37a0e-219">Flags</span></span></th>
<th><span data-ttu-id="37a0e-220">Description</span><span class="sxs-lookup"><span data-stu-id="37a0e-220">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-221">FEED_READY</span><span class="sxs-lookup"><span data-stu-id="37a0e-221">FEED_READY</span></span></td>
<td><span data-ttu-id="37a0e-222">平板可供使用。</span><span class="sxs-lookup"><span data-stu-id="37a0e-222">The flatbed is ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-223">FLAT_READY</span><span class="sxs-lookup"><span data-stu-id="37a0e-223">FLAT_READY</span></span></td>
<td><span data-ttu-id="37a0e-224">掃描器在平板玻璃上有一份檔。</span><span class="sxs-lookup"><span data-stu-id="37a0e-224">The scanner has a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-225">DUP_READY</span><span class="sxs-lookup"><span data-stu-id="37a0e-225">DUP_READY</span></span></td>
<td><span data-ttu-id="37a0e-226">自動列印器已啟用且可供使用。</span><span class="sxs-lookup"><span data-stu-id="37a0e-226">The duplexer is enabled and ready to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-227">FLAT_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="37a0e-227">FLAT_COVER_UP</span></span></td>
<td><span data-ttu-id="37a0e-228">平坦的床朝上。</span><span class="sxs-lookup"><span data-stu-id="37a0e-228">The flat bed cover is up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-229">PATH_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="37a0e-229">PATH_COVER_UP</span></span></td>
<td><span data-ttu-id="37a0e-230">涵蓋的是檔路徑，並導致無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="37a0e-230">The paper path is covered up and is preventing proper operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-231">PAPER_JAM</span><span class="sxs-lookup"><span data-stu-id="37a0e-231">PAPER_JAM</span></span></td>
<td><span data-ttu-id="37a0e-232">檔送紙器中的檔已卡住。</span><span class="sxs-lookup"><span data-stu-id="37a0e-232">A document is jammed in the document feeder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-233">FILM_TPA_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-233">FILM_TPA_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="37a0e-234">已安裝並準備好使用「透明度介面卡」。</span><span class="sxs-lookup"><span data-stu-id="37a0e-234">The transparency adapter is installed and ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-235">STORAGE_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-235">STORAGE_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="37a0e-236">內部儲存體裝置已準備就緒。</span><span class="sxs-lookup"><span data-stu-id="37a0e-236">The internal storage device is ready.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-237">STORAGE_FULL<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-237">STORAGE_FULL<strong>V</strong></span></span></td>
<td><span data-ttu-id="37a0e-238">儲存體已滿，無法進行上傳作業。</span><span class="sxs-lookup"><span data-stu-id="37a0e-238">The storage is full, no upload operations possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-239">MULTIPLE_FEED<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-239">MULTIPLE_FEED<strong>V</strong></span></span></td>
<td><span data-ttu-id="37a0e-240">發生多個摘要條件 (通常會有 PAPER_JAM) 。</span><span class="sxs-lookup"><span data-stu-id="37a0e-240">A multiple feed condition occurred (usually with a PAPER_JAM).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-241">DEVICE_ATTENTION<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-241">DEVICE_ATTENTION<strong>V</strong></span></span></td>
<td><span data-ttu-id="37a0e-242">發生錯誤，需要使用者在裝置上介入。</span><span class="sxs-lookup"><span data-stu-id="37a0e-242">There is an error that requires user intervention on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-243">LAMP_ERR<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-243">LAMP_ERR<strong>V</strong></span></span></td>
<td><span data-ttu-id="37a0e-244">掃描器未就緒，因為發生燈泡問題。</span><span class="sxs-lookup"><span data-stu-id="37a0e-244">The scanner is not ready due to a lamp problem.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <span data-ttu-id="37a0e-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-246">包含應用程式可用於建立有效 endorser 字串的所有有效字元。</span><span class="sxs-lookup"><span data-stu-id="37a0e-246">Contains all the valid characters that an application can use to create valid endorser strings.</span></span> <span data-ttu-id="37a0e-247">Endorser 是安裝在掃描器上的印表機，可在每個掃描的頁面上 imprints 文字訊息。</span><span class="sxs-lookup"><span data-stu-id="37a0e-247">An endorser is a printer installed on a scanner that imprints a text message on every page scanned.</span></span> <span data-ttu-id="37a0e-248">迷你驅動程式應該針對這個屬性中的有效字元集驗證 <strong>WIA_DPS_ENDORSER_STRING</strong> 屬性的設定。</span><span class="sxs-lookup"><span data-stu-id="37a0e-248">The minidriver should validate the setting of the <strong>WIA_DPS_ENDORSER_STRING</strong> property against the valid character set in this property.</span></span> <span data-ttu-id="37a0e-249">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-249">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-250">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-250">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <span data-ttu-id="37a0e-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-252">包含要背書的字串 (換句話說，在迷你驅動程式掃描的每個頁面上列印) 。</span><span class="sxs-lookup"><span data-stu-id="37a0e-252">Contains a string that is to be endorsed (in other words, printed) on each page that the minidriver scans.</span></span> <span data-ttu-id="37a0e-253">應用程式會使用 <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> 屬性中所報告的有效字元集來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-253">An application sets this property using the valid character set that is reported in the <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> property.</span></span> <span data-ttu-id="37a0e-254">只有在這個屬性中設定了字串時，迷你驅動程式才會將檔背書。</span><span class="sxs-lookup"><span data-stu-id="37a0e-254">The minidriver should endorse documents only if a string is set in this property.</span></span> <span data-ttu-id="37a0e-255">空字串表示 endorser 功能已停用。</span><span class="sxs-lookup"><span data-stu-id="37a0e-255">An empty string means that the endorser functionality is disabled.</span></span></p>
<p><span data-ttu-id="37a0e-256">因為驅動程式必須負責解讀 endorser 字串，所以您的驅動程式可以在 <strong>WIA_DPS_ENDORSER_STRING</strong>中使用特殊字元。</span><span class="sxs-lookup"><span data-stu-id="37a0e-256">Because it is the driver's responsibility to interpret the endorser string, your driver can use special characters in <strong>WIA_DPS_ENDORSER_STRING</strong>.</span></span> <span data-ttu-id="37a0e-257">不過，只有您的應用程式會瞭解這些字元。</span><span class="sxs-lookup"><span data-stu-id="37a0e-257">However, only your applications would understand these characters.</span></span></p>
<p><span data-ttu-id="37a0e-258">Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-258">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-259">支援 <strong>WIA_DPS_ENDORSER_STRING</strong> 屬性的驅動程式必須支援下列權杖清單。</span><span class="sxs-lookup"><span data-stu-id="37a0e-259">A driver supporting the <strong>WIA_DPS_ENDORSER_STRING</strong> property must support the following list of tokens.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-260">Token</span><span class="sxs-lookup"><span data-stu-id="37a0e-260">Token</span></span></th>
<th><span data-ttu-id="37a0e-261">描述</span><span class="sxs-lookup"><span data-stu-id="37a0e-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-262">$DATE $</span><span class="sxs-lookup"><span data-stu-id="37a0e-262">$DATE$</span></span></td>
<td><span data-ttu-id="37a0e-263">格式為 YYYY/MM/DD 的日期。</span><span class="sxs-lookup"><span data-stu-id="37a0e-263">The date in the form YYYY/MM/DD.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-264">$DAY $</span><span class="sxs-lookup"><span data-stu-id="37a0e-264">$DAY$</span></span></td>
<td><span data-ttu-id="37a0e-265">以 DD 形式的日。</span><span class="sxs-lookup"><span data-stu-id="37a0e-265">The day in the form DD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-266">$MONTH $</span><span class="sxs-lookup"><span data-stu-id="37a0e-266">$MONTH$</span></span></td>
<td><span data-ttu-id="37a0e-267">年份的月份，格式為 MM。</span><span class="sxs-lookup"><span data-stu-id="37a0e-267">The month of the year in the form MM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-268">$PAGE _COUNT $</span><span class="sxs-lookup"><span data-stu-id="37a0e-268">$PAGE_COUNT$</span></span></td>
<td><span data-ttu-id="37a0e-269">傳送的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="37a0e-269">The number of pages transferred.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-270">$TIME $</span><span class="sxs-lookup"><span data-stu-id="37a0e-270">$TIME$</span></span></td>
<td><span data-ttu-id="37a0e-271">一天中的時間，格式為 HH： MM： SS。</span><span class="sxs-lookup"><span data-stu-id="37a0e-271">The time of day in the form HH:MM:SS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-272">$YEAR $</span><span class="sxs-lookup"><span data-stu-id="37a0e-272">$YEAR$</span></span></td>
<td><span data-ttu-id="37a0e-273">YYYY 格式的年份。</span><span class="sxs-lookup"><span data-stu-id="37a0e-273">The year in the form YYYY.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <span data-ttu-id="37a0e-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-275">保留，請勿使用。</span><span class="sxs-lookup"><span data-stu-id="37a0e-275">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="37a0e-276">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <span data-ttu-id="37a0e-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-278">只有在 Windows Vista 和更新版本上才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-278">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-279">包含 web 服務掃描器裝置的 SOAP 位址。</span><span class="sxs-lookup"><span data-stu-id="37a0e-279">Contains the SOAP address of a web services scanner device.</span></span> <span data-ttu-id="37a0e-280">WIA 2.0 迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-280">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-281">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-281">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <span data-ttu-id="37a0e-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-283">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-283">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-284">包含放置於平板之檔的註冊或水準對齊。</span><span class="sxs-lookup"><span data-stu-id="37a0e-284">Contains the registration, or horizontal alignment, for documents placed on the flatbed.</span></span> <span data-ttu-id="37a0e-285">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-285">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-286">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-286">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-287">下表有三個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-287">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-288">常數</span><span class="sxs-lookup"><span data-stu-id="37a0e-288">Constant</span></span></th>
<th><span data-ttu-id="37a0e-289">描述</span><span class="sxs-lookup"><span data-stu-id="37a0e-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-290">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="37a0e-290">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="37a0e-291">這份檔會保持整齊。</span><span class="sxs-lookup"><span data-stu-id="37a0e-291">The paper is left justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-292">中心</span><span class="sxs-lookup"><span data-stu-id="37a0e-292">CENTERED</span></span></td>
<td><span data-ttu-id="37a0e-293">這份檔是中心的。</span><span class="sxs-lookup"><span data-stu-id="37a0e-293">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-294">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="37a0e-294">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="37a0e-295">紙張靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="37a0e-295">The paper is right justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="37a0e-296"><strong>另請參閱</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-296"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="37a0e-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <span data-ttu-id="37a0e-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-299">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-299">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="37a0e-300">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-301">指定在水準 (X) 軸掃描的最大寬度（以英寸為限），從平台掃描器的滾筒到目前的解析度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-301">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="37a0e-302">這個屬性也適用于將工作表移至平台掃描器的影印以進行掃描的自動檔送紙程式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-302">This property also applies to automatic document feeders that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="37a0e-303">具有玻璃的掃描器必須有這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-303">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="37a0e-304">其他掃描器類型會改為執行 <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-304">Other scanner types will instead implement the <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="37a0e-305">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-305">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="37a0e-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-307">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-307">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="37a0e-308">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-309">指定從掌上 (X) 軸掃描的最大寬度（以英寸為限），以目前解析度的掌上型或紙紙掃描器進行掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-309">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="37a0e-310">這個屬性也適用于自動檔的自動檔，不需要將工作表移至平台掃描器的滾筒就能進行掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-310">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="37a0e-311">這是工作表、捲軸和手入掃描器的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-311">This property is mandatory for sheet-fed, scroll-fed, and hand-held scanners.</span></span></p>
<p><span data-ttu-id="37a0e-312">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <span data-ttu-id="37a0e-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-314">包含使用目前的屬性設定掃描單一頁面的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-314">Contains the maximum time to scan a single page with the current property settings, in milliseconds.</span></span> <span data-ttu-id="37a0e-315">應用程式會讀取此屬性，以估計掃描頁面所需的時間。</span><span class="sxs-lookup"><span data-stu-id="37a0e-315">An application reads this property to estimate the time it will take to scan a page.</span></span> <span data-ttu-id="37a0e-316">這在判斷已停止回應之裝置的條件時很有説明。</span><span class="sxs-lookup"><span data-stu-id="37a0e-316">This is helpful when determining the conditions of a device that has stopped responding.</span></span> <span data-ttu-id="37a0e-317">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-317">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="37a0e-318">所有掃描器都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-318">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="37a0e-319">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-319">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="37a0e-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-321">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-321">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="37a0e-322">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-323">包含掃描器檔送紙器可掃描之最小頁面的實體水準維度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-323">Contains the physical horizontal dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="37a0e-324">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-324">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-325">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-325">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-326"><strong>另請參閱</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-326"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="37a0e-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="37a0e-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-329">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-329">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="37a0e-330">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-331">包含掃描器檔送紙器可掃描之最小頁面的實體垂直尺寸（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-331">Contains the physical vertical dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="37a0e-332">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-332">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-333">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-333">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-334"><strong>另請參閱</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-334"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="37a0e-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <span data-ttu-id="37a0e-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-337">Windows Vista 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-337">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="37a0e-338">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-339">水準光學解析度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-339">Horizontal Optical Resolution.</span></span> <span data-ttu-id="37a0e-340">最高支援的水準光學解析度（DPI）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-340">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="37a0e-341">這個屬性是單一值。</span><span class="sxs-lookup"><span data-stu-id="37a0e-341">This property is a single value.</span></span> <span data-ttu-id="37a0e-342">這不是可由裝置產生的所有解決方案的清單。</span><span class="sxs-lookup"><span data-stu-id="37a0e-342">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="37a0e-343">相反地，這是裝置光纖的解析度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-343">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="37a0e-344">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-344">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="37a0e-345">所有掃描器都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-345">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="37a0e-346">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-346">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <span data-ttu-id="37a0e-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-348">Windows Vista 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-348">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="37a0e-349">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-350">垂直光學解析度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-350">Vertical Optical Resolution.</span></span> <span data-ttu-id="37a0e-351">支援的最高垂直光學解析度（DPI）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-351">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="37a0e-352">這個屬性是單一值。</span><span class="sxs-lookup"><span data-stu-id="37a0e-352">This property is a single value.</span></span> <span data-ttu-id="37a0e-353">這不是裝置產生的所有解決方案的清單。</span><span class="sxs-lookup"><span data-stu-id="37a0e-353">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="37a0e-354">相反地，這是裝置光纖的解析度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-354">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="37a0e-355">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-355">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="37a0e-356">所有掃描器都需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-356">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="37a0e-357">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-357">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <span data-ttu-id="37a0e-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-359">包含目前的方向設定。迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-359">Contains the current orientation setting.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-360">應用程式會設定 <strong>WIA_DPS_ORIENTATION</strong> 屬性，以定義要取得之頁面或影像的原始方向。</span><span class="sxs-lookup"><span data-stu-id="37a0e-360">An application sets the <strong>WIA_DPS_ORIENTATION</strong> property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="37a0e-361">如需如何使用 WIA_DPS_ORIENTATION 的詳細資訊，請參閱 <strong>WIA_DPS_PAGE_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-361">For information on how to use WIA_DPS_ORIENTATION, see <strong>WIA_DPS_PAGE_SIZE</strong></span></span></p>
<p><span data-ttu-id="37a0e-362">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-362">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="37a0e-363">下表包含四個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-363">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-364">值</span><span class="sxs-lookup"><span data-stu-id="37a0e-364">Value</span></span></th>
<th><span data-ttu-id="37a0e-365">定義</span><span class="sxs-lookup"><span data-stu-id="37a0e-365">Defination</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-366">景觀</span><span class="sxs-lookup"><span data-stu-id="37a0e-366">LANDSCAPE</span></span></td>
<td><span data-ttu-id="37a0e-367">相對於直向的順向計數器旋轉旋轉。90</span><span class="sxs-lookup"><span data-stu-id="37a0e-367">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-368">肖像</span><span class="sxs-lookup"><span data-stu-id="37a0e-368">PORTRAIT</span></span></td>
<td><span data-ttu-id="37a0e-369">0度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-369">0 degrees.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-370">ROT180</span><span class="sxs-lookup"><span data-stu-id="37a0e-370">ROT180</span></span></td>
<td><span data-ttu-id="37a0e-371">相對於直向的順向計數器旋轉旋轉。180</span><span class="sxs-lookup"><span data-stu-id="37a0e-371">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-372">ROT270</span><span class="sxs-lookup"><span data-stu-id="37a0e-372">ROT270</span></span></td>
<td><span data-ttu-id="37a0e-373">相對於直向的順向計數器旋轉旋轉。270</span><span class="sxs-lookup"><span data-stu-id="37a0e-373">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="37a0e-374"><strong>另請參閱</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-374"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="37a0e-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="37a0e-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <span data-ttu-id="37a0e-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-377">當沒有足夠的影像資料來填滿要求的緩衝區時，用來填補的色彩。</span><span class="sxs-lookup"><span data-stu-id="37a0e-377">Color used to pad when there is not enough image data to fill a requested buffer.</span></span> <span data-ttu-id="37a0e-378">這個屬性是針對填補緩衝區的掃描器所執行。</span><span class="sxs-lookup"><span data-stu-id="37a0e-378">This property is implemented for scanners that pad the buffer.</span></span> <span data-ttu-id="37a0e-379">所有掃描器的這個屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="37a0e-379">This property is optional for all scanners.</span></span> <span data-ttu-id="37a0e-380">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-380">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-381">類型： <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-381">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-382">色彩資訊的格式為 <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-382">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <span data-ttu-id="37a0e-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-384">Windows Vista 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-384">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="37a0e-385">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-386">包含目前所選頁面的高度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-386">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="37a0e-387">迷你驅動程式會建立並維護 <strong>WIA_DPS_PAGE_HEIGHT</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-387">The minidriver creates and maintains the <strong>WIA_DPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="37a0e-388">應用程式會讀取此屬性，以判斷所掃描之頁面的實體維度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-388">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="37a0e-389">如果範圍設定與已知的頁面大小不同，這個屬性會報告頁面的高度，其 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM (這是 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性) 的值。</span><span class="sxs-lookup"><span data-stu-id="37a0e-389">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_DPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="37a0e-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> 必須與 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>同步，以報告要掃描之頁面的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> must be in sync with <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="37a0e-391">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <span data-ttu-id="37a0e-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-393">Windows Vista 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-393">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="37a0e-394">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-395">包含目前已選取要掃描的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="37a0e-395">Contains the size of the page that is currently selected to be scanned.</span></span> <span data-ttu-id="37a0e-396">若要選取要掃描的頁面維度，應用程式會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-396">To select the dimensions of the page to scan, an application sets this property.</span></span> <span data-ttu-id="37a0e-397">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-397">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-398">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-398">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="37a0e-399">下表有三個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-399">The following table has the three constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-400">值</span><span class="sxs-lookup"><span data-stu-id="37a0e-400">Value</span></span></th>
<th><span data-ttu-id="37a0e-401">定義</span><span class="sxs-lookup"><span data-stu-id="37a0e-401">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-402">WIA_PAGE_A4</span><span class="sxs-lookup"><span data-stu-id="37a0e-402">WIA_PAGE_A4</span></span></td>
<td><span data-ttu-id="37a0e-403">8267 X 11692 (縱向方向) </span><span class="sxs-lookup"><span data-stu-id="37a0e-403">8267 X 11692 (PORTRAIT orientation)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-404">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="37a0e-404">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="37a0e-405">由 <strong>WIA_DPS_PAGE_HEIGHT</strong> 的值和 <strong>WIA_DPS_PAGE_WIDTH</strong> 屬性定義</span><span class="sxs-lookup"><span data-stu-id="37a0e-405">Defined by the values of the <strong>WIA_DPS_PAGE_HEIGHT</strong> and <strong>WIA_DPS_PAGE_WIDTH</strong> properties</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-406">WIA_PAGE_LETTER</span><span class="sxs-lookup"><span data-stu-id="37a0e-406">WIA_PAGE_LETTER</span></span></td>
<td><span data-ttu-id="37a0e-407">8500 X 11000 (縱向方向) </span><span class="sxs-lookup"><span data-stu-id="37a0e-407">8500 X 11000 (PORTRAIT orientation)</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="37a0e-408"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>屬性的值會決定目前選取之頁面的方向。</span><span class="sxs-lookup"><span data-stu-id="37a0e-408">The value of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="37a0e-409"><strong>WIA_DPS_PAGE_WIDTH</strong>和<strong>WIA_DPS_PAGE_HEIGHT</strong>屬性會報告頁面的尺寸（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-409">The <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="37a0e-410">請注意，這些屬性必須與 <strong>WIA_IPS_XEXTENT</strong> 和 <strong>WIA_IPS_YEXTENT</strong>一致，其中包含頁面的尺寸（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-410">Note that these properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span> <span data-ttu-id="37a0e-411">WIA_PROP_LIST 類型的有效值應取決於 <strong>WIA_IPS_ORIENTATION</strong> 屬性的有效設定。</span><span class="sxs-lookup"><span data-stu-id="37a0e-411">Valid values of type WIA_PROP_LIST should depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="37a0e-412">如果裝置無法使用 WIA_PAGE_A4 設定來掃描橫向導向的檔，當<strong>WIA_IPS_ORIENTATION</strong>設為 LANSCAPE 時，WIA_PAGE_A4 不應該出現在<strong>WIA_DPS_PAGE_SIZE</strong>屬性的有效值清單中。</span><span class="sxs-lookup"><span data-stu-id="37a0e-412">If the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 should not appear in the list of valid values for the <strong>WIA_DPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANSCAPE.</span></span></p>
<p><span data-ttu-id="37a0e-413">如果應用程式將 <strong>WIA_DPS_PAGE_SIZE</strong> 設定為 WIA_PAGE_CUSTOM 以外的任何值，則迷你驅動程式應該調整 <strong>WIA_DPS_PAGE_WIDTH</strong> 的值，並 <strong>WIA_DPS_PAGE_HEIGHT</strong> 為頁面的尺寸（以英寸為萬分之一）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-413">If an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to any value other than WIA_PAGE_CUSTOM, the minidriver should adjust the values of <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="37a0e-414">它也應該調整 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> 的值，並 <strong>WIA_IPS_YEXTENT</strong> 為頁面的尺寸（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-414">It should also adjust the values of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="37a0e-415">如果範圍設定 (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> 或 <strong>WIA_IPS_YEXTENT</strong>) 變更為不符合目前頁面大小設定的值，則迷你驅動程式應該將 [ <strong>WIA_DPS_PAGE_SIZE</strong> ] 屬性的值變更為 [WIA_PAGE_CUSTOM]。</span><span class="sxs-lookup"><span data-stu-id="37a0e-415">If an extent setting (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page-size setting, the minidriver should change the value of the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="37a0e-416">迷你驅動程式也應該根據新的範圍設定來修改 <strong>WIA_DPS_PAGE_WIDTH</strong> 或 <strong>WIA_DPS_PAGE_HEIGHT</strong> 。</span><span class="sxs-lookup"><span data-stu-id="37a0e-416">The minidriver should also modify <strong>WIA_DPS_PAGE_WIDTH</strong> or <strong>WIA_DPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="37a0e-417">如果 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> 設定為 LANSCAPE，則會翻轉範圍設定 &quot; 。 &quot; 例如，如果應用程式將 <strong>WIA_DPS_PAGE_SIZE</strong> 設定為 WIA_PAGE_A4，迷你驅動程式應該將 <strong>WIA_DPS_PAGE_WIDTH</strong> 設定為11692，並將 <strong>WIA_DPS_PAGE_HEIGHT</strong> 設定為8267。</span><span class="sxs-lookup"><span data-stu-id="37a0e-417">If <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> is set to LANSCAPE, the extent settings will be &quot;flipped.&quot; For example, if an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver should set <strong>WIA_DPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_DPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="37a0e-418"> (迷你驅動程式也應該設定 <strong>WIA_IPS_XEXTENT</strong> ，並據此 <strong>WIA_IPS_YEXTENT</strong> 。 ) 請注意，如果 <strong>WIA_DPS_PAGE_SIZE</strong> 設定為 WIA_PAGE_CUSTOM，則方向設定不會用來判斷要掃描之頁面的範圍維度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-418">(The minidriver should also set <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.) Note that if <strong>WIA_DPS_PAGE_SIZE</strong> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span></p>
<p><span data-ttu-id="37a0e-419">迷你驅動程式負責確保 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> 屬性與目前的選取區域一致。</span><span class="sxs-lookup"><span data-stu-id="37a0e-419">The minidriver is responsible for ensuring that the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property is in agreement with the current selection area.</span></span> <span data-ttu-id="37a0e-420">如果應用程式將 <strong>WIA_IPS_ORIENTATION</strong> 的值變更為目前選取之頁面大小不正確值，則迷你驅動程式應該將 <strong>WIA_DPS_PAGE_SIZE</strong> 的值變更為新的方向值所支援的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="37a0e-420">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_DPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="37a0e-421">如果應用程式將 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM，則目前的選取範圍不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="37a0e-421">If an application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="37a0e-422">WIA 迷你驅動程式應該會從目前的 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> 設定開始，取得目前的影像版面配置，並 <strong>WIA_IPS_YPOS</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-422">The WIA minidriver should obtain the current image layout, starting from the current settings of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="37a0e-423">如果頁面大小設定產生掃描器外的選取區域，則迷你驅動程式必須自動調整 <strong>WIA_IPS_XPOS</strong> 的值，並 <strong>WIA_IPS_YPOS</strong> 屬性設定為有效的設定。</span><span class="sxs-lookup"><span data-stu-id="37a0e-423">If the page-size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="37a0e-424">如果 <strong>WIA_DPS_PAGE_SIZE</strong> 和 <strong>WIA_IPS_ORIENTATION</strong> 屬性同時設定，且在組合套用時無效，則迷你驅動程式應該會在 <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv：:d rvvalidateitemproperties</a>中傳回錯誤，以使應用程式的設定失敗。</span><span class="sxs-lookup"><span data-stu-id="37a0e-424">If the <strong>WIA_DPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span> <span data-ttu-id="37a0e-425">.</span><span class="sxs-lookup"><span data-stu-id="37a0e-425">.</span></span></p>
<p><span data-ttu-id="37a0e-426">下列四個範例顯示不同 <strong>WIA_DPS_PAGE_SIZE</strong> 案例。</span><span class="sxs-lookup"><span data-stu-id="37a0e-426">The following four examples show different <strong>WIA_DPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="37a0e-427">驅動程式會報告設定。</span><span class="sxs-lookup"><span data-stu-id="37a0e-427">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="37a0e-428">應用程式會將 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_LETTER。</span><span class="sxs-lookup"><span data-stu-id="37a0e-428">An application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="37a0e-429">應用程式會將 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> 屬性設定為 LANSCAPE。</span><span class="sxs-lookup"><span data-stu-id="37a0e-429">An application sets the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property to LANSCAPE.</span></span></li>
<li><span data-ttu-id="37a0e-430">應用程式會將 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> 屬性變更為較小的值。</span><span class="sxs-lookup"><span data-stu-id="37a0e-430">An application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="37a0e-431"><strong>範例1：迷你驅動程式報告設定</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-431"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="37a0e-432">在下列範例中，迷你驅動程式會在應用程式設定任何 WIA 屬性之前，設定自訂選取區域。</span><span class="sxs-lookup"><span data-stu-id="37a0e-432">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="37a0e-433">在此情況下，選取區域代表整個平板。</span><span class="sxs-lookup"><span data-stu-id="37a0e-433">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
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
<p><span data-ttu-id="37a0e-434"><strong>範例2：應用程式將</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>屬性設定為 WIA_PAGE_LETTER</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-434"><strong>Example 2: An application sets the</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
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
<p><span data-ttu-id="37a0e-435"><strong>範例3：應用程式將</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>屬性設定為 LANSCAPE</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-435"><strong>Example 3: An application sets the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>property to LANSCAPE</strong></span></span></p>
<p><span data-ttu-id="37a0e-436">實體床必須能夠取得原本處於橫向方向的頁面。</span><span class="sxs-lookup"><span data-stu-id="37a0e-436">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<p><span data-ttu-id="37a0e-437"><strong>範例4：應用程式</strong>將 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>屬性變更為較小的值</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-437"><strong>Example 4: An application changes the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="37a0e-438">在下列範例中，應用程式會將 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> 屬性變更為1000。</span><span class="sxs-lookup"><span data-stu-id="37a0e-438">In the following example, an application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to 1000.</span></span> <span data-ttu-id="37a0e-439">迷你驅動程式應該假設 <strong>WIA_IPS_XEXTENT</strong> 中包含的新值不再適用于 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性，因此應該將 <strong>WIA_DPS_PAGE_SIZE</strong> 變更為 WIA_PAGE_CUSTOM。</span><span class="sxs-lookup"><span data-stu-id="37a0e-439">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_DPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="37a0e-440">迷你驅動程式也必須調整 <strong>WIA_DPS_PAGE_WIDTH</strong>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-440">The minidriver must also adjust <strong>WIA_DPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <span data-ttu-id="37a0e-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-442">Windows Vista 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-442">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="37a0e-443">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-444">包含目前所選取頁面的寬度（以英寸為限）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-444">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="37a0e-445">應用程式會讀取此屬性，以判斷所掃描之頁面的實體維度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-445">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="37a0e-446">如果範圍設定與已知的頁面大小不同，這個屬性會報告頁面的寬度，其 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM。</span><span class="sxs-lookup"><span data-stu-id="37a0e-446">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="37a0e-447"><strong>WIA_DPS_PAGE_WIDTH</strong> 必須與 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>的值同步，這會報告要掃描頁面的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-447"><strong>WIA_DPS_PAGE_WIDTH</strong> must be in sync with the value of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="37a0e-448">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-448">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-449">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-449">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <span data-ttu-id="37a0e-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-451">Windows Vista 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-451">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="37a0e-452">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-453">包含要從自動檔送紙器取得的目前頁面數目。</span><span class="sxs-lookup"><span data-stu-id="37a0e-453">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="37a0e-454">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-454">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-455">類型： <strong>VT_I4</strong>;存取：讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (零到檔送紙器可以容納的最大頁面數目) </span><span class="sxs-lookup"><span data-stu-id="37a0e-455">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero through the maximum number of pages that the document feeder can hold)</span></span></p>
<p><span data-ttu-id="37a0e-456">應用程式會讀取此屬性，以判斷檔送紙器的頁面容量。</span><span class="sxs-lookup"><span data-stu-id="37a0e-456">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="37a0e-457">應用程式也會將此屬性設定為要掃描的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="37a0e-457">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-458">如果已啟用雙工模式 (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> 設定為 [送紙器] |雙工 ) ， <strong>WIA_DPS_PAGES</strong> 仍等於要掃描的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="37a0e-458">If duplex mode is enabled (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-459">如果已啟用雙工，則會自動包含兩頁的紙張，即使頁面的後端是空白的。</span><span class="sxs-lookup"><span data-stu-id="37a0e-459">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="37a0e-460">將 <strong>WIA_DPS_PAGES</strong> 設定為1，會導致掃描器處理頁面的其中一個邊。</span><span class="sxs-lookup"><span data-stu-id="37a0e-460">Setting <strong>WIA_DPS_PAGES</strong> to 1 causes a scanner to process one of the sides of the page.</span></span> <span data-ttu-id="37a0e-461">如果掃描器在雙工模式下無法僅掃描頁面的一端，則應該將 WIA_PROPERTY_INFO 結構的 Inc 成員 <strong>WIA_DPS_PAGES</strong> 有效值變更為2。</span><span class="sxs-lookup"><span data-stu-id="37a0e-461">It is recommended that if a scanner is unable to scan only one side of a page while in duplex mode, the <strong>WIA_DPS_PAGES</strong> valid value for the Inc member of the WIA_PROPERTY_INFO structure should be changed to 2.</span></span> <span data-ttu-id="37a0e-462">此值會通知應用程式，它必須以兩個的倍數要求頁面。</span><span class="sxs-lookup"><span data-stu-id="37a0e-462">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="37a0e-463">值為零表示要掃描目前載入檔送紙器中的 <em>所有</em> 頁面。</span><span class="sxs-lookup"><span data-stu-id="37a0e-463">A value of zero means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <span data-ttu-id="37a0e-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-465">指定要掃描的工作表背面的影印色彩。</span><span class="sxs-lookup"><span data-stu-id="37a0e-465">Specifies the color of the platen in back of the sheet to be scanned.</span></span> <span data-ttu-id="37a0e-466">對於具有玻璃的掃描器，這個屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="37a0e-466">This property is optional for scanners that have a platen.</span></span> <span data-ttu-id="37a0e-467">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-467">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-468">類型： <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-468">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-469">色彩資訊的格式為 <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-469">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <span data-ttu-id="37a0e-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-471">Windows Vista 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-471">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="37a0e-472">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-473">指出裝置的預覽模式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-473">Indicates the preview mode for a device.</span></span> <span data-ttu-id="37a0e-474">應用程式會設定此屬性，以將裝置置於預覽模式。</span><span class="sxs-lookup"><span data-stu-id="37a0e-474">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="37a0e-475">Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-475">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="37a0e-476">下表有兩個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-476">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-477">值</span><span class="sxs-lookup"><span data-stu-id="37a0e-477">Value</span></span></th>
<th><span data-ttu-id="37a0e-478">定義</span><span class="sxs-lookup"><span data-stu-id="37a0e-478">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-479">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="37a0e-479">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="37a0e-480">應用程式將會執行最後的掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-480">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-481">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="37a0e-481">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="37a0e-482">應用程式將會執行預覽掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-482">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <span data-ttu-id="37a0e-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="37a0e-484">包含值，指出掃描器在將頁面傳送至應用程式之前，是否會在掃描器緩衝區中快取頁面。</span><span class="sxs-lookup"><span data-stu-id="37a0e-484">Contains a value that indicates whether the scanner will cache pages in a scanner buffer before sending them to the application.</span></span></p>
<p><span data-ttu-id="37a0e-485">值為0會停用事先掃描，而且不會事先掃描任何頁面。</span><span class="sxs-lookup"><span data-stu-id="37a0e-485">A value of zero disables scan ahead and no pages will be scanned ahead.</span></span> <span data-ttu-id="37a0e-486">在經過緩衝處理的掃描專案上進行一般資料傳輸，會抓取緩衝的頁面。</span><span class="sxs-lookup"><span data-stu-id="37a0e-486">Doing normal data transfers on the buffered scan-ahead item retrieves the buffered pages.</span></span> <span data-ttu-id="37a0e-487">在提前掃描工作期間，無法變更 WIA 屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-487">WIA properties cannot be changed during a scan-ahead operation.</span></span> <span data-ttu-id="37a0e-488">這是選用屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-488">This property is optional.</span></span></p>
<p><span data-ttu-id="37a0e-489">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值：從零到檔送紙器可以容納的最大頁面數目的 <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 。</span><span class="sxs-lookup"><span data-stu-id="37a0e-489">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <span data-ttu-id="37a0e-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-491">只有 Windows 7 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-491">This property is supported only by Windows 7 and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-492">指出輸入來源 (平板、自動檔送紙器或 fil 掃描介面卡) 進行掃描，或要從中傳送資料的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="37a0e-492">Indicates the input source (flatbed, automatic document feeder, or fil-scanning adapter) to scan from, or the storage location to transfer data from.</span></span></p>
<p><span data-ttu-id="37a0e-493">掃描事件會通知應用程式使用者已啟動掃描，但該事件未提供代表輸入來源之 WIA 專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="37a0e-493">A scan event notifies the application that the user has initiated a scan, but the event does not supply the name of the WIA item that represents the input source.</span></span> <span data-ttu-id="37a0e-494">應用程式的事件處理常式可以查詢根專案的 WIA_DPS_SCAN_AVAILABLE_ITEM 屬性，以取得輸入來源專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="37a0e-494">The application's event handler can query the root item's WIA_DPS_SCAN_AVAILABLE_ITEM property to get the name of the input source item.</span></span></p>
<p><span data-ttu-id="37a0e-495">類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值：從零到檔送紙器可以容納的最大頁面數目的 <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 。</span><span class="sxs-lookup"><span data-stu-id="37a0e-495">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <span data-ttu-id="37a0e-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-497">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-497">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-498">包含 Web 服務掃描器裝置的服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="37a0e-498">Contains the Service ID of a Web Services scanner device.</span></span> <span data-ttu-id="37a0e-499">WIA 2.0 迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-499">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-500">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-500">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <span data-ttu-id="37a0e-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-502">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-502">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="37a0e-503">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-504">包含放置於平板之檔的註冊（或對齊和邊緣偵測）。</span><span class="sxs-lookup"><span data-stu-id="37a0e-504">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="37a0e-505">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-505">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="37a0e-506">這個屬性會指出工作表如何水準定位於掌上型或紙匣掃描器的掃描標頭上。</span><span class="sxs-lookup"><span data-stu-id="37a0e-506">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="37a0e-507">屬性是用來預測檔放置於掃描標頭的哪個位置。</span><span class="sxs-lookup"><span data-stu-id="37a0e-507">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="37a0e-508">如果掃描器支援一個以上的掃描標頭，這個屬性會相對於最上層的掃描標頭。</span><span class="sxs-lookup"><span data-stu-id="37a0e-508">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="37a0e-509">這是工作表、捲軸和掌上型掃描器的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-509">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="37a0e-510">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-510">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-511">下表有三個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-511">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-512">常數</span><span class="sxs-lookup"><span data-stu-id="37a0e-512">Constant</span></span></th>
<th><span data-ttu-id="37a0e-513">描述</span><span class="sxs-lookup"><span data-stu-id="37a0e-513">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-514">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="37a0e-514">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="37a0e-515">工作表在掃描標頭的相對位置。</span><span class="sxs-lookup"><span data-stu-id="37a0e-515">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-516">中心</span><span class="sxs-lookup"><span data-stu-id="37a0e-516">CENTERED</span></span></td>
<td><span data-ttu-id="37a0e-517">工作表會以掃描標頭為中心。</span><span class="sxs-lookup"><span data-stu-id="37a0e-517">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-518">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="37a0e-518">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="37a0e-519">工作表位於掃描標頭的右邊。</span><span class="sxs-lookup"><span data-stu-id="37a0e-519">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <span data-ttu-id="37a0e-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-521">Windows Vista 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-521">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="37a0e-522">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-523">指出專案是否需要向使用者顯示預覽控制項。</span><span class="sxs-lookup"><span data-stu-id="37a0e-523">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="37a0e-524">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-524">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-525">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-525">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-526">下表有兩個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-526">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-527">常數</span><span class="sxs-lookup"><span data-stu-id="37a0e-527">Constant</span></span></th>
<th><span data-ttu-id="37a0e-528">描述</span><span class="sxs-lookup"><span data-stu-id="37a0e-528">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-529">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="37a0e-529">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="37a0e-530">顯示使用者的預覽控制項，因為此裝置可以執行預覽。</span><span class="sxs-lookup"><span data-stu-id="37a0e-530">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="37a0e-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="37a0e-532">不要向使用者顯示預覽控制項，因為此裝置無法執行預覽。</span><span class="sxs-lookup"><span data-stu-id="37a0e-532">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <span data-ttu-id="37a0e-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-534">只有 Windows Vista 和更新版本才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-534">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-535">由 WIA 服務用來通知迷你驅動程式有關使用者帳戶名稱 (包括目前 WIA 應用程式執行所在會話的可用) 的網路功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="37a0e-535">Used by the WIA service to inform the mini-driver about the user account name (including the network domain name when applicable) of the session in which the current WIA application is running.</span></span></p>
<p><span data-ttu-id="37a0e-536">這是由 WIA 服務管理的根專案屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-536">This is a root item property, managed by the WIA service.</span></span></p>
<p><span data-ttu-id="37a0e-537">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-537">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <span data-ttu-id="37a0e-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-539">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-539">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-540">包含放置於平板之檔的註冊或垂直對齊和邊緣偵測。</span><span class="sxs-lookup"><span data-stu-id="37a0e-540">Contains the registration, or vertical alignment and edge detection, for documents placed on the flatbed.</span></span> <span data-ttu-id="37a0e-541">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-541">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="37a0e-542">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-542">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="37a0e-543">下表有三個對此屬性有效的常數。</span><span class="sxs-lookup"><span data-stu-id="37a0e-543">The following table has the three constants that are valid with this property..</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="37a0e-544">常數</span><span class="sxs-lookup"><span data-stu-id="37a0e-544">Constant</span></span></th>
<th><span data-ttu-id="37a0e-545">描述</span><span class="sxs-lookup"><span data-stu-id="37a0e-545">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a0e-546">TOP_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="37a0e-546">TOP_JUSTIFIED</span></span></td>
<td><span data-ttu-id="37a0e-547">這份白皮書最重要。</span><span class="sxs-lookup"><span data-stu-id="37a0e-547">The paper is top justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a0e-548">中心</span><span class="sxs-lookup"><span data-stu-id="37a0e-548">CENTERED</span></span></td>
<td><span data-ttu-id="37a0e-549">這份檔是中心的。</span><span class="sxs-lookup"><span data-stu-id="37a0e-549">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a0e-550">BOTTOM_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="37a0e-550">BOTTOM_JUSTIFIED</span></span></td>
<td><span data-ttu-id="37a0e-551">這份白皮書靠下對齊。</span><span class="sxs-lookup"><span data-stu-id="37a0e-551">The paper is bottom justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="37a0e-552">另<strong>請參閱</strong>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-552"><strong>See Also</strong>.</span></span></p>
<p><span data-ttu-id="37a0e-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="37a0e-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <span data-ttu-id="37a0e-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-555">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-555">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="37a0e-556">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-557">指定在垂直 (Y) 軸中掃描的最大高度（以英寸為限），從平台掃描器的滾筒到目前的解析度。</span><span class="sxs-lookup"><span data-stu-id="37a0e-557">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="37a0e-558">這個屬性也適用于自動檔送紙程式，可將工作表移至平台掃描器的影印以進行掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-558">This property also applies to automatic document feeders, that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="37a0e-559">具有玻璃的掃描器必須有這個屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-559">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="37a0e-560">其他掃描器類型會改為執行 <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> 屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-560">Other scanner types will instead implement the <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="37a0e-561">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="37a0e-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="37a0e-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a0e-563">Windows Vista 和更新版本不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-563">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="37a0e-564">使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="37a0e-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="37a0e-565">指定在垂直 (Y) 軸的最大高度（以英寸為間隔），從掌上型或工作表饋送掃描器以目前的解析度掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-565">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="37a0e-566">這個屬性也適用于自動檔的自動檔，不需要將工作表移至平台掃描器的滾筒就能進行掃描。</span><span class="sxs-lookup"><span data-stu-id="37a0e-566">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="37a0e-567">這是工作表饋送掃描器的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-567">This property is mandatory for sheet-fed scanners.</span></span> <span data-ttu-id="37a0e-568">滾動饋送和掌上型掃描器不應執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="37a0e-568">Scroll-fed and hand-held scanners should not implement this property.</span></span></p>
<p><span data-ttu-id="37a0e-569">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="37a0e-569">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="37a0e-570">規格需求</span><span class="sxs-lookup"><span data-stu-id="37a0e-570">Requirements</span></span>



| <span data-ttu-id="37a0e-571">需求</span><span class="sxs-lookup"><span data-stu-id="37a0e-571">Requirement</span></span> | <span data-ttu-id="37a0e-572">值</span><span class="sxs-lookup"><span data-stu-id="37a0e-572">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37a0e-573">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37a0e-573">Minimum supported client</span></span><br/> | <span data-ttu-id="37a0e-574">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37a0e-574">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="37a0e-575">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37a0e-575">Minimum supported server</span></span><br/> | <span data-ttu-id="37a0e-576">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37a0e-576">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="37a0e-577">標頭</span><span class="sxs-lookup"><span data-stu-id="37a0e-577">Header</span></span><br/>                   | <dl> <span data-ttu-id="37a0e-578"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="37a0e-578"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
