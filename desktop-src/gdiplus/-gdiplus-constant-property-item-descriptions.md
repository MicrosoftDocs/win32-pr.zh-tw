---
description: 下列清單提供 Windows GDI + 所支援之屬性專案的描述。
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: 屬性專案描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636120"
---
# <a name="property-item-descriptions"></a><span data-ttu-id="70d6c-103">屬性專案描述</span><span class="sxs-lookup"><span data-stu-id="70d6c-103">Property Item Descriptions</span></span>

<span data-ttu-id="70d6c-104">下列清單提供 Windows GDI + 所支援之屬性專案的描述。</span><span class="sxs-lookup"><span data-stu-id="70d6c-104">The following list gives descriptions of the property items supported by Windows GDI+.</span></span> <span data-ttu-id="70d6c-105">描述很簡單且一般，因此適用于各種不同的影像檔案格式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-105">The descriptions are brief and general so that they apply to a variety of image file formats.</span></span> <span data-ttu-id="70d6c-106">如需特定檔案格式如何使用屬性專案的詳細說明，請參閱該檔案格式的規格。</span><span class="sxs-lookup"><span data-stu-id="70d6c-106">For a detailed description of how a property item is used by a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="70d6c-107">如需詳細描述中繼資料之多個檔案規格和其他檔的連結，請參閱 [影像檔案格式規格](-gdiplus-constant-image-file-format-specifications.md)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-107">For links to several file specifications and other documents that describe metadata in detail, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span>

<span data-ttu-id="70d6c-108"> (EXIF) 格式的交換影像檔是日本的電子產業開發關聯 (JEIDA) standard，1998年6月修改為2.1 版。</span><span class="sxs-lookup"><span data-stu-id="70d6c-108">The Exchangeable Image File (EXIF) format is a Japan Electronic Industry Development Association (JEIDA) standard, revised June 1998 as version 2.1.</span></span> <span data-ttu-id="70d6c-109">EXIF 規格的部分是與 JEIDA 的許可權一起使用。</span><span class="sxs-lookup"><span data-stu-id="70d6c-109">Portions of the EXIF specification are used with permission of JEIDA.</span></span>

## <a name="propertytaggpsver"></a><span data-ttu-id="70d6c-110">PropertyTagGpsVer</span><span class="sxs-lookup"><span data-stu-id="70d6c-110">PropertyTagGpsVer</span></span>

<span data-ttu-id="70d6c-111">全球定位系統的版本 (GPS) IFD，指定為2.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="70d6c-111">Version of the Global Positioning Systems (GPS) IFD, given as 2.0.0.0.</span></span> <span data-ttu-id="70d6c-112">當 PropertyTagGpsIFD 標記存在時，此標記是必要的。</span><span class="sxs-lookup"><span data-stu-id="70d6c-112">This tag is mandatory when the PropertyTagGpsIFD tag is present.</span></span> <span data-ttu-id="70d6c-113">當版本為2.0.0.0 時，標記值為0x02000000。</span><span class="sxs-lookup"><span data-stu-id="70d6c-113">When the version is 2.0.0.0, the tag value is 0x02000000.</span></span>



| <span data-ttu-id="70d6c-114">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-114">Property info</span></span> | <span data-ttu-id="70d6c-115">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-115">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-116">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-116">Tag</span></span>   | <span data-ttu-id="70d6c-117">0x0000</span><span class="sxs-lookup"><span data-stu-id="70d6c-117">0x0000</span></span>              |
| <span data-ttu-id="70d6c-118">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-118">Type</span></span>  | <span data-ttu-id="70d6c-119">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-119">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="70d6c-120">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-120">Count</span></span> | <span data-ttu-id="70d6c-121">4</span><span class="sxs-lookup"><span data-stu-id="70d6c-121">4</span></span>                   |



 

## <a name="propertytaggpslatituderef"></a><span data-ttu-id="70d6c-122">PropertyTagGpsLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-122">PropertyTagGpsLatitudeRef</span></span>

<span data-ttu-id="70d6c-123">以 Null 結束的字元字串，指定緯度為北方或南部。</span><span class="sxs-lookup"><span data-stu-id="70d6c-123">Null-terminated character string that specifies whether the latitude is north or south.</span></span> <span data-ttu-id="70d6c-124">`N` 指定北美洲緯度，並 `S` 指定南部緯度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-124">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="70d6c-125">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-125">Property info</span></span> | <span data-ttu-id="70d6c-126">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-126">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-127">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-127">Tag</span></span>   | <span data-ttu-id="70d6c-128">0x0001</span><span class="sxs-lookup"><span data-stu-id="70d6c-128">0x0001</span></span>                                     |
| <span data-ttu-id="70d6c-129">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-129">Type</span></span>  | <span data-ttu-id="70d6c-130">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-130">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-131">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-131">Count</span></span> | <span data-ttu-id="70d6c-132">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-132">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslatitude"></a><span data-ttu-id="70d6c-133">PropertyTagGpsLatitude</span><span class="sxs-lookup"><span data-stu-id="70d6c-133">PropertyTagGpsLatitude</span></span>

<span data-ttu-id="70d6c-134">緯度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-134">Latitude.</span></span> <span data-ttu-id="70d6c-135">緯度表示為三個值，分別提供度數、分和秒。</span><span class="sxs-lookup"><span data-stu-id="70d6c-135">Latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="70d6c-136">當表示度、分和秒時，格式為 dd/1、mm/1、ss/1。</span><span class="sxs-lookup"><span data-stu-id="70d6c-136">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="70d6c-137">使用度和分鐘時，例如分數的分鐘數最多可達兩位數，格式為 dd/1、mmmm/100、0/1。</span><span class="sxs-lookup"><span data-stu-id="70d6c-137">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="70d6c-138">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-138">Property info</span></span> | <span data-ttu-id="70d6c-139">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-139">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-140">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-140">Tag</span></span>   | <span data-ttu-id="70d6c-141">0x0002</span><span class="sxs-lookup"><span data-stu-id="70d6c-141">0x0002</span></span>                  |
| <span data-ttu-id="70d6c-142">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-142">Type</span></span>  | <span data-ttu-id="70d6c-143">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-143">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-144">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-144">Count</span></span> | <span data-ttu-id="70d6c-145">3</span><span class="sxs-lookup"><span data-stu-id="70d6c-145">3</span></span>                       |



 

## <a name="propertytaggpslongituderef"></a><span data-ttu-id="70d6c-146">PropertyTagGpsLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-146">PropertyTagGpsLongitudeRef</span></span>

<span data-ttu-id="70d6c-147">以 Null 結束的字元字串，指定經度是東或西經度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-147">Null-terminated character string that specifies whether the longitude is east or west longitude.</span></span> <span data-ttu-id="70d6c-148">`E` 指定東部經度，並 `W` 指定 west 經度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-148">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="70d6c-149">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-149">Property info</span></span> | <span data-ttu-id="70d6c-150">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-150">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-151">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-151">Tag</span></span>   | <span data-ttu-id="70d6c-152">0x0003</span><span class="sxs-lookup"><span data-stu-id="70d6c-152">0x0003</span></span>                                     |
| <span data-ttu-id="70d6c-153">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-153">Type</span></span>  | <span data-ttu-id="70d6c-154">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-154">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-155">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-155">Count</span></span> | <span data-ttu-id="70d6c-156">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-156">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslongitude"></a><span data-ttu-id="70d6c-157">PropertyTagGpsLongitude</span><span class="sxs-lookup"><span data-stu-id="70d6c-157">PropertyTagGpsLongitude</span></span>

<span data-ttu-id="70d6c-158">經度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-158">Longitude.</span></span> <span data-ttu-id="70d6c-159">經度表示為三個值，分別提供度數、分和秒。</span><span class="sxs-lookup"><span data-stu-id="70d6c-159">Longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="70d6c-160">當表示度、分和秒時，格式為 ddd/1、mm/1、ss/1。</span><span class="sxs-lookup"><span data-stu-id="70d6c-160">When degrees, minutes and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="70d6c-161">使用度和分鐘時，例如分數的分鐘數最多可達兩位數，格式為 ddd/1、mmmm/100、0/1。</span><span class="sxs-lookup"><span data-stu-id="70d6c-161">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="70d6c-162">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-162">Property info</span></span> | <span data-ttu-id="70d6c-163">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-163">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-164">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-164">Tag</span></span>   | <span data-ttu-id="70d6c-165">0x0004</span><span class="sxs-lookup"><span data-stu-id="70d6c-165">0x0004</span></span>                  |
| <span data-ttu-id="70d6c-166">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-166">Type</span></span>  | <span data-ttu-id="70d6c-167">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-167">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-168">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-168">Count</span></span> | <span data-ttu-id="70d6c-169">3</span><span class="sxs-lookup"><span data-stu-id="70d6c-169">3</span></span>                       |



 

## <a name="propertytaggpsaltituderef"></a><span data-ttu-id="70d6c-170">PropertyTagGpsAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-170">PropertyTagGpsAltitudeRef</span></span>

<span data-ttu-id="70d6c-171">參考高度，以計量為單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-171">Reference altitude, in meters.</span></span>



| <span data-ttu-id="70d6c-172">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-172">Property info</span></span> | <span data-ttu-id="70d6c-173">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-173">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-174">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-174">Tag</span></span>   | <span data-ttu-id="70d6c-175">0x0005</span><span class="sxs-lookup"><span data-stu-id="70d6c-175">0x0005</span></span>              |
| <span data-ttu-id="70d6c-176">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-176">Type</span></span>  | <span data-ttu-id="70d6c-177">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-177">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="70d6c-178">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-178">Count</span></span> | <span data-ttu-id="70d6c-179">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-179">1</span></span>                   |



 

## <a name="propertytaggpsaltitude"></a><span data-ttu-id="70d6c-180">PropertyTagGpsAltitude</span><span class="sxs-lookup"><span data-stu-id="70d6c-180">PropertyTagGpsAltitude</span></span>

<span data-ttu-id="70d6c-181">高度（以量為單位），以 PropertyTagGpsAltitudeRef 所指定的參考高度為基礎。</span><span class="sxs-lookup"><span data-stu-id="70d6c-181">Altitude, in meters, based on the reference altitude specified by PropertyTagGpsAltitudeRef.</span></span>



| <span data-ttu-id="70d6c-182">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-182">Property info</span></span> | <span data-ttu-id="70d6c-183">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-183">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-184">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-184">Tag</span></span>   | <span data-ttu-id="70d6c-185">0x0006</span><span class="sxs-lookup"><span data-stu-id="70d6c-185">0x0006</span></span>                  |
| <span data-ttu-id="70d6c-186">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-186">Type</span></span>  | <span data-ttu-id="70d6c-187">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-187">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-188">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-188">Count</span></span> | <span data-ttu-id="70d6c-189">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-189">1</span></span>                       |



 

## <a name="propertytaggpsgpstime"></a><span data-ttu-id="70d6c-190">PropertyTagGpsGpsTime</span><span class="sxs-lookup"><span data-stu-id="70d6c-190">PropertyTagGpsGpsTime</span></span>

<span data-ttu-id="70d6c-191">國際標準時間 (UTC) 的時間。</span><span class="sxs-lookup"><span data-stu-id="70d6c-191">Time as Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="70d6c-192">此值會以三個指定小時、分和秒的有理數表示。</span><span class="sxs-lookup"><span data-stu-id="70d6c-192">The value is expressed as three rational numbers that give the hour, minute, and second.</span></span>



| <span data-ttu-id="70d6c-193">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-193">Property info</span></span> | <span data-ttu-id="70d6c-194">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-194">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-195">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-195">Tag</span></span>   | <span data-ttu-id="70d6c-196">0x0007</span><span class="sxs-lookup"><span data-stu-id="70d6c-196">0x0007</span></span>                  |
| <span data-ttu-id="70d6c-197">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-197">Type</span></span>  | <span data-ttu-id="70d6c-198">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-198">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-199">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-199">Count</span></span> | <span data-ttu-id="70d6c-200">3</span><span class="sxs-lookup"><span data-stu-id="70d6c-200">3</span></span>                       |



 

## <a name="propertytaggpsgpssatellites"></a><span data-ttu-id="70d6c-201">PropertyTagGpsGpsSatellites</span><span class="sxs-lookup"><span data-stu-id="70d6c-201">PropertyTagGpsGpsSatellites</span></span>

<span data-ttu-id="70d6c-202">以 Null 結束的字元字串，指定用於測量的 GPS 附屬元件。</span><span class="sxs-lookup"><span data-stu-id="70d6c-202">Null-terminated character string that specifies the GPS satellites used for measurements.</span></span> <span data-ttu-id="70d6c-203">此標記可用來指定識別碼、提高許可權的角度、azimuth、SNR，以及有關每個附屬的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-203">This tag can be used to specify the ID number, angle of elevation, azimuth, SNR, and other information about each satellite.</span></span> <span data-ttu-id="70d6c-204">未指定格式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-204">The format is not specified.</span></span> <span data-ttu-id="70d6c-205">如果 GPS 接收者無法進行度量，則必須將標記的值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="70d6c-205">If the GPS receiver is incapable of taking measurements, the value of the tag must be set to **NULL**.</span></span>



| <span data-ttu-id="70d6c-206">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-206">Property info</span></span> | <span data-ttu-id="70d6c-207">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-207">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-208">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-208">Tag</span></span>   | <span data-ttu-id="70d6c-209">0x0008</span><span class="sxs-lookup"><span data-stu-id="70d6c-209">0x0008</span></span>                                             |
| <span data-ttu-id="70d6c-210">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-210">Type</span></span>  | <span data-ttu-id="70d6c-211">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-211">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-212">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-212">Count</span></span> | <span data-ttu-id="70d6c-213">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-213">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsgpsstatus"></a><span data-ttu-id="70d6c-214">PropertyTagGpsGpsStatus</span><span class="sxs-lookup"><span data-stu-id="70d6c-214">PropertyTagGpsGpsStatus</span></span>

<span data-ttu-id="70d6c-215">以 Null 結束的字元字串，這個字串會指定記錄影像時 GPS 接收器的狀態。</span><span class="sxs-lookup"><span data-stu-id="70d6c-215">Null-terminated character string that specifies the status of the GPS receiver when the image is recorded.</span></span> <span data-ttu-id="70d6c-216">`A` 表示正在進行測量， `V` 表示測量是互通性。</span><span class="sxs-lookup"><span data-stu-id="70d6c-216">`A` means measurement is in progress, and `V` means the measurement is Interoperability.</span></span>



| <span data-ttu-id="70d6c-217">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-217">Property info</span></span> | <span data-ttu-id="70d6c-218">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-218">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-219">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-219">Tag</span></span>   | <span data-ttu-id="70d6c-220">0x0009</span><span class="sxs-lookup"><span data-stu-id="70d6c-220">0x0009</span></span>                                     |
| <span data-ttu-id="70d6c-221">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-221">Type</span></span>  | <span data-ttu-id="70d6c-222">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-222">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-223">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-223">Count</span></span> | <span data-ttu-id="70d6c-224">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-224">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsmeasuremode"></a><span data-ttu-id="70d6c-225">PropertyTagGpsGpsMeasureMode</span><span class="sxs-lookup"><span data-stu-id="70d6c-225">PropertyTagGpsGpsMeasureMode</span></span>

<span data-ttu-id="70d6c-226">以 Null 結束的字元字串，指定 GPS 測量模式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-226">Null-terminated character string that specifies the GPS measurement mode.</span></span> <span data-ttu-id="70d6c-227">`2` 指定2D 測量，並 `3` 指定立體度量。</span><span class="sxs-lookup"><span data-stu-id="70d6c-227">`2` specifies 2-D measurement, and `3` specifies 3-D measurement.</span></span>



| <span data-ttu-id="70d6c-228">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-228">Property info</span></span> | <span data-ttu-id="70d6c-229">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-229">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-230">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-230">Tag</span></span>   | <span data-ttu-id="70d6c-231">0x000A</span><span class="sxs-lookup"><span data-stu-id="70d6c-231">0x000A</span></span>                                     |
| <span data-ttu-id="70d6c-232">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-232">Type</span></span>  | <span data-ttu-id="70d6c-233">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-233">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-234">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-234">Count</span></span> | <span data-ttu-id="70d6c-235">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-235">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsdop"></a><span data-ttu-id="70d6c-236">PropertyTagGpsGpsDop</span><span class="sxs-lookup"><span data-stu-id="70d6c-236">PropertyTagGpsGpsDop</span></span>

<span data-ttu-id="70d6c-237">GPS DOP (精確度) 的資料程度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-237">GPS DOP (data degree of precision).</span></span> <span data-ttu-id="70d6c-238">HDOP 值是在2D 測量期間寫入，而 PDOP 值則是在立體測量期間寫入。</span><span class="sxs-lookup"><span data-stu-id="70d6c-238">An HDOP value is written during 2-D measurement, and a PDOP value is written during 3-D measurement.</span></span>



| <span data-ttu-id="70d6c-239">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-239">Property info</span></span> | <span data-ttu-id="70d6c-240">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-240">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-241">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-241">Tag</span></span>   | <span data-ttu-id="70d6c-242">0x000B</span><span class="sxs-lookup"><span data-stu-id="70d6c-242">0x000B</span></span>                  |
| <span data-ttu-id="70d6c-243">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-243">Type</span></span>  | <span data-ttu-id="70d6c-244">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-244">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-245">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-245">Count</span></span> | <span data-ttu-id="70d6c-246">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-246">1</span></span>                       |



 

## <a name="propertytaggpsspeedref"></a><span data-ttu-id="70d6c-247">PropertyTagGpsSpeedRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-247">PropertyTagGpsSpeedRef</span></span>

<span data-ttu-id="70d6c-248">以 Null 結束的字元字串，指定用來表示移動 GPS 接收器速度的單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-248">Null-terminated character string that specifies the unit used to express the GPS receiver speed of movement.</span></span> <span data-ttu-id="70d6c-249">`K`、 `M` 和 `N` 分別代表每小時公里、每小時英里和節點。</span><span class="sxs-lookup"><span data-stu-id="70d6c-249">`K`, `M`, and `N` represent kilometers per hour, miles per hour, and knots respectively.</span></span>



| <span data-ttu-id="70d6c-250">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-250">Property info</span></span> | <span data-ttu-id="70d6c-251">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-251">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-252">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-252">Tag</span></span>   | <span data-ttu-id="70d6c-253">0x000C</span><span class="sxs-lookup"><span data-stu-id="70d6c-253">0x000C</span></span>                                     |
| <span data-ttu-id="70d6c-254">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-254">Type</span></span>  | <span data-ttu-id="70d6c-255">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-255">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-256">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-256">Count</span></span> | <span data-ttu-id="70d6c-257">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-257">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsspeed"></a><span data-ttu-id="70d6c-258">PropertyTagGpsSpeed</span><span class="sxs-lookup"><span data-stu-id="70d6c-258">PropertyTagGpsSpeed</span></span>

<span data-ttu-id="70d6c-259">GPS 接收器移動的速度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-259">Speed of the GPS receiver movement.</span></span>



| <span data-ttu-id="70d6c-260">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-260">Property info</span></span> | <span data-ttu-id="70d6c-261">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-261">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-262">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-262">Tag</span></span>   | <span data-ttu-id="70d6c-263">0x000D</span><span class="sxs-lookup"><span data-stu-id="70d6c-263">0x000D</span></span>                  |
| <span data-ttu-id="70d6c-264">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-264">Type</span></span>  | <span data-ttu-id="70d6c-265">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-265">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-266">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-266">Count</span></span> | <span data-ttu-id="70d6c-267">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-267">1</span></span>                       |



 

## <a name="propertytaggpstrackref"></a><span data-ttu-id="70d6c-268">PropertyTagGpsTrackRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-268">PropertyTagGpsTrackRef</span></span>

<span data-ttu-id="70d6c-269">以 Null 結束的字元字串，指定用來提供 GPS 接收器移動方向的參考。</span><span class="sxs-lookup"><span data-stu-id="70d6c-269">Null-terminated character string that specifies the reference for giving the direction of GPS receiver movement.</span></span> <span data-ttu-id="70d6c-270">`T` 指定 true 方向，並 `M` 指定磁性方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-270">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="70d6c-271">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-271">Property info</span></span> | <span data-ttu-id="70d6c-272">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-272">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-273">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-273">Tag</span></span>   | <span data-ttu-id="70d6c-274">0x000E</span><span class="sxs-lookup"><span data-stu-id="70d6c-274">0x000E</span></span>                                     |
| <span data-ttu-id="70d6c-275">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-275">Type</span></span>  | <span data-ttu-id="70d6c-276">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-276">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-277">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-277">Count</span></span> | <span data-ttu-id="70d6c-278">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-278">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpstrack"></a><span data-ttu-id="70d6c-279">PropertyTagGpsTrack</span><span class="sxs-lookup"><span data-stu-id="70d6c-279">PropertyTagGpsTrack</span></span>

<span data-ttu-id="70d6c-280">GPS 接收器移動的方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-280">Direction of GPS receiver movement.</span></span> <span data-ttu-id="70d6c-281">值的範圍是從0.00 到359.99。</span><span class="sxs-lookup"><span data-stu-id="70d6c-281">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="70d6c-282">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-282">Property info</span></span> | <span data-ttu-id="70d6c-283">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-283">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-284">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-284">Tag</span></span>   | <span data-ttu-id="70d6c-285">0x000F</span><span class="sxs-lookup"><span data-stu-id="70d6c-285">0x000F</span></span>                  |
| <span data-ttu-id="70d6c-286">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-286">Type</span></span>  | <span data-ttu-id="70d6c-287">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-287">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-288">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-288">Count</span></span> | <span data-ttu-id="70d6c-289">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-289">1</span></span>                       |



 

## <a name="propertytaggpsimgdirref"></a><span data-ttu-id="70d6c-290">PropertyTagGpsImgDirRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-290">PropertyTagGpsImgDirRef</span></span>

<span data-ttu-id="70d6c-291">以 Null 結束的字元字串，指定在捕獲影像時的參考。</span><span class="sxs-lookup"><span data-stu-id="70d6c-291">Null-terminated character string that specifies the reference for the direction of the image when it is captured.</span></span> <span data-ttu-id="70d6c-292">`T` 指定 true 方向，並 `M` 指定磁性方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-292">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="70d6c-293">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-293">Property info</span></span> | <span data-ttu-id="70d6c-294">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-294">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-295">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-295">Tag</span></span>   | <span data-ttu-id="70d6c-296">0x0010</span><span class="sxs-lookup"><span data-stu-id="70d6c-296">0x0010</span></span>                                     |
| <span data-ttu-id="70d6c-297">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-297">Type</span></span>  | <span data-ttu-id="70d6c-298">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-298">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-299">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-299">Count</span></span> | <span data-ttu-id="70d6c-300">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-300">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsimgdir"></a><span data-ttu-id="70d6c-301">PropertyTagGpsImgDir</span><span class="sxs-lookup"><span data-stu-id="70d6c-301">PropertyTagGpsImgDir</span></span>

<span data-ttu-id="70d6c-302">影像在捕獲時的方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-302">Direction of the image when it was captured.</span></span> <span data-ttu-id="70d6c-303">值的範圍是從0.00 到359.99。</span><span class="sxs-lookup"><span data-stu-id="70d6c-303">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="70d6c-304">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-304">Property info</span></span> | <span data-ttu-id="70d6c-305">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-306">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-306">Tag</span></span>   | <span data-ttu-id="70d6c-307">0x0011</span><span class="sxs-lookup"><span data-stu-id="70d6c-307">0x0011</span></span>                  |
| <span data-ttu-id="70d6c-308">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-308">Type</span></span>  | <span data-ttu-id="70d6c-309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-310">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-310">Count</span></span> | <span data-ttu-id="70d6c-311">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-311">1</span></span>                       |



 

## <a name="propertytaggpsmapdatum"></a><span data-ttu-id="70d6c-312">PropertyTagGpsMapDatum</span><span class="sxs-lookup"><span data-stu-id="70d6c-312">PropertyTagGpsMapDatum</span></span>

<span data-ttu-id="70d6c-313">以 Null 結束的字元字串，指定 GPS 接收器所使用的 geodetic 調查資料。</span><span class="sxs-lookup"><span data-stu-id="70d6c-313">Null-terminated character string that specifies geodetic survey data used by the GPS receiver.</span></span> <span data-ttu-id="70d6c-314">如果問卷資料僅限日本，則此標記的值為 `TOKYO` 或 `WGS-84` 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-314">If the survey data is restricted to Japan, the value of this tag is `TOKYO` or `WGS-84`.</span></span>



| <span data-ttu-id="70d6c-315">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-315">Property info</span></span> | <span data-ttu-id="70d6c-316">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-316">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-317">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-317">Tag</span></span>   | <span data-ttu-id="70d6c-318">0x0012</span><span class="sxs-lookup"><span data-stu-id="70d6c-318">0x0012</span></span>                                             |
| <span data-ttu-id="70d6c-319">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-319">Type</span></span>  | <span data-ttu-id="70d6c-320">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-320">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-321">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-321">Count</span></span> | <span data-ttu-id="70d6c-322">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-322">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsdestlatref"></a><span data-ttu-id="70d6c-323">PropertyTagGpsDestLatRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-323">PropertyTagGpsDestLatRef</span></span>

<span data-ttu-id="70d6c-324">以 Null 結束的字元字串，這個字串會指定目的點的緯度是北或南緯度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-324">Null-terminated character string that specifies whether the latitude of the destination point is north or south latitude.</span></span> <span data-ttu-id="70d6c-325">`N` 指定北美洲緯度，並 `S` 指定南部緯度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-325">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="70d6c-326">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-326">Property info</span></span> | <span data-ttu-id="70d6c-327">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-327">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-328">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-328">Tag</span></span>   | <span data-ttu-id="70d6c-329">0x0013</span><span class="sxs-lookup"><span data-stu-id="70d6c-329">0x0013</span></span>                                     |
| <span data-ttu-id="70d6c-330">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-330">Type</span></span>  | <span data-ttu-id="70d6c-331">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-331">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-332">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-332">Count</span></span> | <span data-ttu-id="70d6c-333">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-333">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlat"></a><span data-ttu-id="70d6c-334">PropertyTagGpsDestLat</span><span class="sxs-lookup"><span data-stu-id="70d6c-334">PropertyTagGpsDestLat</span></span>

<span data-ttu-id="70d6c-335">目的地點的緯度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-335">Latitude of the destination point.</span></span> <span data-ttu-id="70d6c-336">緯度表示為三個值，分別提供度數、分和秒。</span><span class="sxs-lookup"><span data-stu-id="70d6c-336">The latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="70d6c-337">當表示度、分和秒時，格式為 dd/1、mm/1、ss/1。</span><span class="sxs-lookup"><span data-stu-id="70d6c-337">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="70d6c-338">使用度和分鐘時，例如分數的分鐘數最多可達兩位數，格式為 dd/1、mmmm/100、0/1。</span><span class="sxs-lookup"><span data-stu-id="70d6c-338">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="70d6c-339">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-339">Property info</span></span> | <span data-ttu-id="70d6c-340">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-340">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-341">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-341">Tag</span></span>   | <span data-ttu-id="70d6c-342">0x0014</span><span class="sxs-lookup"><span data-stu-id="70d6c-342">0x0014</span></span>                  |
| <span data-ttu-id="70d6c-343">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-343">Type</span></span>  | <span data-ttu-id="70d6c-344">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-344">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-345">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-345">Count</span></span> | <span data-ttu-id="70d6c-346">3</span><span class="sxs-lookup"><span data-stu-id="70d6c-346">3</span></span>                       |



 

## <a name="propertytaggpsdestlongref"></a><span data-ttu-id="70d6c-347">PropertyTagGpsDestLongRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-347">PropertyTagGpsDestLongRef</span></span>

<span data-ttu-id="70d6c-348">以 Null 結束的字元字串，這個字串會指定目的點的經度是東或西經度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-348">Null-terminated character string that specifies whether the longitude of the destination point is east or west longitude.</span></span> <span data-ttu-id="70d6c-349">`E` 指定東部經度，並 `W` 指定 west 經度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-349">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="70d6c-350">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-350">Property info</span></span> | <span data-ttu-id="70d6c-351">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-351">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-352">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-352">Tag</span></span>   | <span data-ttu-id="70d6c-353">0x0015</span><span class="sxs-lookup"><span data-stu-id="70d6c-353">0x0015</span></span>                                     |
| <span data-ttu-id="70d6c-354">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-354">Type</span></span>  | <span data-ttu-id="70d6c-355">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-355">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-356">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-356">Count</span></span> | <span data-ttu-id="70d6c-357">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-357">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlong"></a><span data-ttu-id="70d6c-358">PropertyTagGpsDestLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-358">PropertyTagGpsDestLong</span></span>

<span data-ttu-id="70d6c-359">目的地點的經度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-359">Longitude of the destination point.</span></span> <span data-ttu-id="70d6c-360">經度會表示為三個值，分別提供度數、分和秒。</span><span class="sxs-lookup"><span data-stu-id="70d6c-360">The longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="70d6c-361">當表示度、分和秒時，格式為 ddd/1、mm/1、ss/1。</span><span class="sxs-lookup"><span data-stu-id="70d6c-361">When degrees, minutes, and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="70d6c-362">使用度和分鐘時，例如分數的分鐘數最多可達兩位數，格式為 ddd/1、mmmm/100、0/1。</span><span class="sxs-lookup"><span data-stu-id="70d6c-362">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="70d6c-363">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-363">Property info</span></span> | <span data-ttu-id="70d6c-364">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-364">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-365">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-365">Tag</span></span>   | <span data-ttu-id="70d6c-366">0x0016</span><span class="sxs-lookup"><span data-stu-id="70d6c-366">0x0016</span></span>                  |
| <span data-ttu-id="70d6c-367">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-367">Type</span></span>  | <span data-ttu-id="70d6c-368">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-368">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-369">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-369">Count</span></span> | <span data-ttu-id="70d6c-370">3</span><span class="sxs-lookup"><span data-stu-id="70d6c-370">3</span></span>                       |



 

## <a name="propertytaggpsdestbearref"></a><span data-ttu-id="70d6c-371">PropertyTagGpsDestBearRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-371">PropertyTagGpsDestBearRef</span></span>

<span data-ttu-id="70d6c-372">以 Null 結束的字元字串，指定用來為目的點提供關聯的參考。</span><span class="sxs-lookup"><span data-stu-id="70d6c-372">Null-terminated character string that specifies the reference used for giving the bearing to the destination point.</span></span> <span data-ttu-id="70d6c-373">`T` 指定 true 方向，並 `M` 指定磁性方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-373">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="70d6c-374">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-374">Property info</span></span> | <span data-ttu-id="70d6c-375">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-375">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-376">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-376">Tag</span></span>   | <span data-ttu-id="70d6c-377">0x0017</span><span class="sxs-lookup"><span data-stu-id="70d6c-377">0x0017</span></span>                                     |
| <span data-ttu-id="70d6c-378">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-378">Type</span></span>  | <span data-ttu-id="70d6c-379">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-379">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-380">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-380">Count</span></span> | <span data-ttu-id="70d6c-381">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-381">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestbear"></a><span data-ttu-id="70d6c-382">PropertyTagGpsDestBear</span><span class="sxs-lookup"><span data-stu-id="70d6c-382">PropertyTagGpsDestBear</span></span>

<span data-ttu-id="70d6c-383">與目的地點有關。</span><span class="sxs-lookup"><span data-stu-id="70d6c-383">Bearing to the destination point.</span></span> <span data-ttu-id="70d6c-384">值的範圍是從0.00 到359.99。</span><span class="sxs-lookup"><span data-stu-id="70d6c-384">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="70d6c-385">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-385">Property info</span></span> | <span data-ttu-id="70d6c-386">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-386">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-387">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-387">Tag</span></span>   | <span data-ttu-id="70d6c-388">0x0018</span><span class="sxs-lookup"><span data-stu-id="70d6c-388">0x0018</span></span>                  |
| <span data-ttu-id="70d6c-389">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-389">Type</span></span>  | <span data-ttu-id="70d6c-390">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-390">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-391">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-391">Count</span></span> | <span data-ttu-id="70d6c-392">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-392">1</span></span>                       |



 

## <a name="propertytaggpsdestdistref"></a><span data-ttu-id="70d6c-393">PropertyTagGpsDestDistRef</span><span class="sxs-lookup"><span data-stu-id="70d6c-393">PropertyTagGpsDestDistRef</span></span>

<span data-ttu-id="70d6c-394">以 Null 結束的字元字串，指定用來表示與目的地點距離的單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-394">Null-terminated character string that specifies the unit used to express the distance to the destination point.</span></span> <span data-ttu-id="70d6c-395">K、M 和 N 分別代表公里、英里和節點。</span><span class="sxs-lookup"><span data-stu-id="70d6c-395">K, M, and N represent kilometers, miles, and knots respectively.</span></span>



| <span data-ttu-id="70d6c-396">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-396">Property info</span></span> | <span data-ttu-id="70d6c-397">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-397">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="70d6c-398">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-398">Tag</span></span>   | <span data-ttu-id="70d6c-399">0x0019</span><span class="sxs-lookup"><span data-stu-id="70d6c-399">0x0019</span></span>                                     |
| <span data-ttu-id="70d6c-400">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-400">Type</span></span>  | <span data-ttu-id="70d6c-401">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-401">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="70d6c-402">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-402">Count</span></span> | <span data-ttu-id="70d6c-403">2 (一個字元加上 Null 結束字元) </span><span class="sxs-lookup"><span data-stu-id="70d6c-403">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestdist"></a><span data-ttu-id="70d6c-404">PropertyTagGpsDestDist</span><span class="sxs-lookup"><span data-stu-id="70d6c-404">PropertyTagGpsDestDist</span></span>

<span data-ttu-id="70d6c-405">與目的地點之間的距離。</span><span class="sxs-lookup"><span data-stu-id="70d6c-405">Distance to the destination point.</span></span>



| <span data-ttu-id="70d6c-406">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-406">Property info</span></span> | <span data-ttu-id="70d6c-407">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-407">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-408">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-408">Tag</span></span>   | <span data-ttu-id="70d6c-409">0x001A</span><span class="sxs-lookup"><span data-stu-id="70d6c-409">0x001A</span></span>                  |
| <span data-ttu-id="70d6c-410">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-410">Type</span></span>  | <span data-ttu-id="70d6c-411">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-411">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-412">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-412">Count</span></span> | <span data-ttu-id="70d6c-413">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-413">1</span></span>                       |



 

## <a name="propertytagnewsubfiletype"></a><span data-ttu-id="70d6c-414">PropertyTagNewSubfileType</span><span class="sxs-lookup"><span data-stu-id="70d6c-414">PropertyTagNewSubfileType</span></span>

<span data-ttu-id="70d6c-415">Subfile 中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="70d6c-415">Type of data in a subfile.</span></span>



| <span data-ttu-id="70d6c-416">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-416">Property info</span></span> | <span data-ttu-id="70d6c-417">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-417">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-418">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-418">Tag</span></span>   | <span data-ttu-id="70d6c-419">0x00FE</span><span class="sxs-lookup"><span data-stu-id="70d6c-419">0x00FE</span></span>              |
| <span data-ttu-id="70d6c-420">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-420">Type</span></span>  | <span data-ttu-id="70d6c-421">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-421">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-422">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-422">Count</span></span> | <span data-ttu-id="70d6c-423">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-423">1</span></span>                   |



 

## <a name="propertytagsubfiletype"></a><span data-ttu-id="70d6c-424">PropertyTagSubfileType</span><span class="sxs-lookup"><span data-stu-id="70d6c-424">PropertyTagSubfileType</span></span>

<span data-ttu-id="70d6c-425">Subfile 中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="70d6c-425">Type of data in a subfile.</span></span>



| <span data-ttu-id="70d6c-426">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-426">Property info</span></span> | <span data-ttu-id="70d6c-427">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-427">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-428">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-428">Tag</span></span>   | <span data-ttu-id="70d6c-429">0x00FF</span><span class="sxs-lookup"><span data-stu-id="70d6c-429">0x00FF</span></span>               |
| <span data-ttu-id="70d6c-430">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-430">Type</span></span>  | <span data-ttu-id="70d6c-431">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-431">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-432">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-432">Count</span></span> | <span data-ttu-id="70d6c-433">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-433">1</span></span>                    |



 

## <a name="propertytagimagewidth"></a><span data-ttu-id="70d6c-434">PropertyTagImageWidth</span><span class="sxs-lookup"><span data-stu-id="70d6c-434">PropertyTagImageWidth</span></span>

<span data-ttu-id="70d6c-435">每個資料列的圖元數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-435">Number of pixels per row.</span></span>



| <span data-ttu-id="70d6c-436">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-436">Property info</span></span> | <span data-ttu-id="70d6c-437">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-437">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-438">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-438">Tag</span></span>   | <span data-ttu-id="70d6c-439">0x0100</span><span class="sxs-lookup"><span data-stu-id="70d6c-439">0x0100</span></span>                                      |
| <span data-ttu-id="70d6c-440">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-440">Type</span></span>  | <span data-ttu-id="70d6c-441">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-441">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-442">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-442">Count</span></span> | <span data-ttu-id="70d6c-443">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-443">1</span></span>                                           |



 

## <a name="propertytagimageheight"></a><span data-ttu-id="70d6c-444">PropertyTagImageHeight</span><span class="sxs-lookup"><span data-stu-id="70d6c-444">PropertyTagImageHeight</span></span>

<span data-ttu-id="70d6c-445">圖元資料列的數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-445">Number of pixel rows.</span></span>



| <span data-ttu-id="70d6c-446">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-446">Property info</span></span> | <span data-ttu-id="70d6c-447">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-447">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-448">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-448">Tag</span></span>   | <span data-ttu-id="70d6c-449">0x0101</span><span class="sxs-lookup"><span data-stu-id="70d6c-449">0x0101</span></span>                                      |
| <span data-ttu-id="70d6c-450">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-450">Type</span></span>  | <span data-ttu-id="70d6c-451">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-451">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-452">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-452">Count</span></span> | <span data-ttu-id="70d6c-453">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-453">1</span></span>                                           |



 

## <a name="propertytagbitspersample"></a><span data-ttu-id="70d6c-454">PropertyTagBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="70d6c-454">PropertyTagBitsPerSample</span></span>

<span data-ttu-id="70d6c-455">每個色彩元件的位數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-455">Number of bits per color component.</span></span> <span data-ttu-id="70d6c-456">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-456">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-457">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-457">Property info</span></span> | <span data-ttu-id="70d6c-458">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-458">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-459">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-459">Tag</span></span>   | <span data-ttu-id="70d6c-460">0x0102</span><span class="sxs-lookup"><span data-stu-id="70d6c-460">0x0102</span></span>                                   |
| <span data-ttu-id="70d6c-461">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-461">Type</span></span>  | <span data-ttu-id="70d6c-462">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-462">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="70d6c-463">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-463">Count</span></span> | <span data-ttu-id="70d6c-464">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-464">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagcompression"></a><span data-ttu-id="70d6c-465">PropertyTagCompression</span><span class="sxs-lookup"><span data-stu-id="70d6c-465">PropertyTagCompression</span></span>

<span data-ttu-id="70d6c-466">用於影像資料的壓縮配置。</span><span class="sxs-lookup"><span data-stu-id="70d6c-466">Compression scheme used for the image data.</span></span>



| <span data-ttu-id="70d6c-467">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-467">Property info</span></span> | <span data-ttu-id="70d6c-468">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-468">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-469">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-469">Tag</span></span>   | <span data-ttu-id="70d6c-470">0x0103</span><span class="sxs-lookup"><span data-stu-id="70d6c-470">0x0103</span></span>               |
| <span data-ttu-id="70d6c-471">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-471">Type</span></span>  | <span data-ttu-id="70d6c-472">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-472">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-473">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-473">Count</span></span> | <span data-ttu-id="70d6c-474">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-474">1</span></span>                    |



 

## <a name="propertytagphotometricinterp"></a><span data-ttu-id="70d6c-475">PropertyTagPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="70d6c-475">PropertyTagPhotometricInterp</span></span>

<span data-ttu-id="70d6c-476">圖元資料的轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-476">How pixel data will be interpreted.</span></span>



| <span data-ttu-id="70d6c-477">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-477">Property info</span></span> | <span data-ttu-id="70d6c-478">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-478">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-479">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-479">Tag</span></span>   | <span data-ttu-id="70d6c-480">0x0106</span><span class="sxs-lookup"><span data-stu-id="70d6c-480">0x0106</span></span>               |
| <span data-ttu-id="70d6c-481">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-481">Type</span></span>  | <span data-ttu-id="70d6c-482">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-482">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-483">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-483">Count</span></span> | <span data-ttu-id="70d6c-484">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-484">1</span></span>                    |



 

## <a name="propertytagthreshholding"></a><span data-ttu-id="70d6c-485">PropertyTagThreshHolding</span><span class="sxs-lookup"><span data-stu-id="70d6c-485">PropertyTagThreshHolding</span></span>

<span data-ttu-id="70d6c-486">用來從灰色圖元轉換成黑色和白色圖元的技巧。</span><span class="sxs-lookup"><span data-stu-id="70d6c-486">Technique used to convert from gray pixels to black and white pixels.</span></span>



| <span data-ttu-id="70d6c-487">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-487">Property info</span></span> | <span data-ttu-id="70d6c-488">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-488">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-489">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-489">Tag</span></span>   | <span data-ttu-id="70d6c-490">0x0107</span><span class="sxs-lookup"><span data-stu-id="70d6c-490">0x0107</span></span>               |
| <span data-ttu-id="70d6c-491">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-491">Type</span></span>  | <span data-ttu-id="70d6c-492">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-492">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-493">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-493">Count</span></span> | <span data-ttu-id="70d6c-494">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-494">1</span></span>                    |



 

## <a name="propertytagcellwidth"></a><span data-ttu-id="70d6c-495">PropertyTagCellWidth</span><span class="sxs-lookup"><span data-stu-id="70d6c-495">PropertyTagCellWidth</span></span>

<span data-ttu-id="70d6c-496">遞色或半色調矩陣的寬度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-496">Width of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="70d6c-497">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-497">Property info</span></span> | <span data-ttu-id="70d6c-498">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-498">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-499">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-499">Tag</span></span>   | <span data-ttu-id="70d6c-500">0x0108</span><span class="sxs-lookup"><span data-stu-id="70d6c-500">0x0108</span></span>               |
| <span data-ttu-id="70d6c-501">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-501">Type</span></span>  | <span data-ttu-id="70d6c-502">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-502">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-503">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-503">Count</span></span> | <span data-ttu-id="70d6c-504">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-504">1</span></span>                    |



 

## <a name="propertytagcellheight"></a><span data-ttu-id="70d6c-505">PropertyTagCellHeight</span><span class="sxs-lookup"><span data-stu-id="70d6c-505">PropertyTagCellHeight</span></span>

<span data-ttu-id="70d6c-506">遞色或半色調矩陣的高度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-506">Height of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="70d6c-507">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-507">Property info</span></span> | <span data-ttu-id="70d6c-508">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-508">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-509">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-509">Tag</span></span>   | <span data-ttu-id="70d6c-510">0x0109</span><span class="sxs-lookup"><span data-stu-id="70d6c-510">0x0109</span></span>               |
| <span data-ttu-id="70d6c-511">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-511">Type</span></span>  | <span data-ttu-id="70d6c-512">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-512">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-513">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-513">Count</span></span> | <span data-ttu-id="70d6c-514">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-514">1</span></span>                    |



 

## <a name="propertytagfillorder"></a><span data-ttu-id="70d6c-515">PropertyTagFillOrder</span><span class="sxs-lookup"><span data-stu-id="70d6c-515">PropertyTagFillOrder</span></span>

<span data-ttu-id="70d6c-516">位元組中位的邏輯順序。</span><span class="sxs-lookup"><span data-stu-id="70d6c-516">Logical order of bits in a byte.</span></span>



| <span data-ttu-id="70d6c-517">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-517">Property info</span></span> | <span data-ttu-id="70d6c-518">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-518">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-519">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-519">Tag</span></span>   | <span data-ttu-id="70d6c-520">0x010A</span><span class="sxs-lookup"><span data-stu-id="70d6c-520">0x010A</span></span>               |
| <span data-ttu-id="70d6c-521">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-521">Type</span></span>  | <span data-ttu-id="70d6c-522">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-522">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-523">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-523">Count</span></span> | <span data-ttu-id="70d6c-524">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-524">1</span></span>                    |



 

## <a name="propertytagdocumentname"></a><span data-ttu-id="70d6c-525">PropertyTagDocumentName</span><span class="sxs-lookup"><span data-stu-id="70d6c-525">PropertyTagDocumentName</span></span>

<span data-ttu-id="70d6c-526">以 Null 結束的字元字串，指定掃描影像的檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="70d6c-526">Null-terminated character string that specifies the name of the document from which the image was scanned.</span></span>



| <span data-ttu-id="70d6c-527">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-527">Property info</span></span> | <span data-ttu-id="70d6c-528">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-528">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-529">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-529">Tag</span></span>   | <span data-ttu-id="70d6c-530">0x010D</span><span class="sxs-lookup"><span data-stu-id="70d6c-530">0x010D</span></span>                                             |
| <span data-ttu-id="70d6c-531">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-531">Type</span></span>  | <span data-ttu-id="70d6c-532">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-532">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-533">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-533">Count</span></span> | <span data-ttu-id="70d6c-534">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-534">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagimagedescription"></a><span data-ttu-id="70d6c-535">PropertyTagImageDescription</span><span class="sxs-lookup"><span data-stu-id="70d6c-535">PropertyTagImageDescription</span></span>

<span data-ttu-id="70d6c-536">以 Null 結束的字元字串，指定影像的標題。</span><span class="sxs-lookup"><span data-stu-id="70d6c-536">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="70d6c-537">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-537">Property info</span></span> | <span data-ttu-id="70d6c-538">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-538">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-539">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-539">Tag</span></span>   | <span data-ttu-id="70d6c-540">0x010E</span><span class="sxs-lookup"><span data-stu-id="70d6c-540">0x010E</span></span>                                             |
| <span data-ttu-id="70d6c-541">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-541">Type</span></span>  | <span data-ttu-id="70d6c-542">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-542">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-543">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-543">Count</span></span> | <span data-ttu-id="70d6c-544">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-544">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmake"></a><span data-ttu-id="70d6c-545">PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="70d6c-545">PropertyTagEquipMake</span></span>

<span data-ttu-id="70d6c-546">以 Null 結束的字元字串，指定用來錄製影像之設備的製造商。</span><span class="sxs-lookup"><span data-stu-id="70d6c-546">Null-terminated character string that specifies the manufacturer of the equipment used to record the image.</span></span>



| <span data-ttu-id="70d6c-547">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-547">Property info</span></span> | <span data-ttu-id="70d6c-548">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-548">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-549">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-549">Tag</span></span>   | <span data-ttu-id="70d6c-550">0x010F</span><span class="sxs-lookup"><span data-stu-id="70d6c-550">0x010F</span></span>                                             |
| <span data-ttu-id="70d6c-551">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-551">Type</span></span>  | <span data-ttu-id="70d6c-552">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-552">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-553">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-553">Count</span></span> | <span data-ttu-id="70d6c-554">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-554">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmodel"></a><span data-ttu-id="70d6c-555">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="70d6c-555">PropertyTagEquipModel</span></span>

<span data-ttu-id="70d6c-556">以 Null 結束的字元字串，指定用來錄製影像之設備的模型名稱或模型編號。</span><span class="sxs-lookup"><span data-stu-id="70d6c-556">Null-terminated character string that specifies the model name or model number of the equipment used to record the image.</span></span>



| <span data-ttu-id="70d6c-557">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-557">Property info</span></span> | <span data-ttu-id="70d6c-558">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-558">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-559">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-559">Tag</span></span>   | <span data-ttu-id="70d6c-560">0x0110</span><span class="sxs-lookup"><span data-stu-id="70d6c-560">0x0110</span></span>                                             |
| <span data-ttu-id="70d6c-561">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-561">Type</span></span>  | <span data-ttu-id="70d6c-562">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-562">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-563">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-563">Count</span></span> | <span data-ttu-id="70d6c-564">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-564">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagstripoffsets"></a><span data-ttu-id="70d6c-565">PropertyTagStripOffsets</span><span class="sxs-lookup"><span data-stu-id="70d6c-565">PropertyTagStripOffsets</span></span>

<span data-ttu-id="70d6c-566">針對每個區域，該區域的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-566">For each strip, the byte offset of that strip.</span></span> <span data-ttu-id="70d6c-567">另請參閱 [PropertyTagRowsPerStrip](#propertytagrowsperstrip) 和 [PropertyTagStripBytesCount](#propertytagstripbytescount)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-567">See also [PropertyTagRowsPerStrip](#propertytagrowsperstrip) and [PropertyTagStripBytesCount](#propertytagstripbytescount).</span></span>



| <span data-ttu-id="70d6c-568">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-568">Property info</span></span> | <span data-ttu-id="70d6c-569">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-569">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-570">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-570">Tag</span></span>   | <span data-ttu-id="70d6c-571">0x0111</span><span class="sxs-lookup"><span data-stu-id="70d6c-571">0x0111</span></span>                                      |
| <span data-ttu-id="70d6c-572">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-572">Type</span></span>  | <span data-ttu-id="70d6c-573">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-573">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-574">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-574">Count</span></span> | <span data-ttu-id="70d6c-575">停車數</span><span class="sxs-lookup"><span data-stu-id="70d6c-575">Number of strips</span></span>                            |



 

## <a name="propertytagorientation"></a><span data-ttu-id="70d6c-576">PropertyTagOrientation</span><span class="sxs-lookup"><span data-stu-id="70d6c-576">PropertyTagOrientation</span></span>

<span data-ttu-id="70d6c-577">根據資料列和資料行來觀看影像方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-577">Image orientation viewed in terms of rows and columns.</span></span>



<span data-ttu-id="70d6c-578">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-578">Tag</span></span>

<span data-ttu-id="70d6c-579">0x0112</span><span class="sxs-lookup"><span data-stu-id="70d6c-579">0x0112</span></span>

<span data-ttu-id="70d6c-580">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-580">Type</span></span>

<span data-ttu-id="70d6c-581">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-581">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-582">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-582">Count</span></span>

<span data-ttu-id="70d6c-583">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-583">1</span></span>

<span data-ttu-id="70d6c-584">1-第0個數據列位於視覺影像的頂端，而第0個數據行則是視覺效果左側。</span><span class="sxs-lookup"><span data-stu-id="70d6c-584">1 - The 0th row is at the top of the visual image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="70d6c-585">2-第0個數據列位於影像的視覺頂端，而第0個數據行則是視覺效果右邊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-585">2 - The 0th row is at the visual top of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="70d6c-586">3-第0個數據列位於影像的視覺底部，而第0個數據行則是視覺效果右邊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-586">3 - The 0th row is at the visual bottom of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="70d6c-587">4-第0個數據列位於影像的視覺底部，而第0個數據行則是視覺效果左側。</span><span class="sxs-lookup"><span data-stu-id="70d6c-587">4 - The 0th row is at the visual bottom of the image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="70d6c-588">5-第0個數據列是影像的視覺位置，而第0個數據行則是視覺效果上方。</span><span class="sxs-lookup"><span data-stu-id="70d6c-588">5 - The 0th row is the visual left side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="70d6c-589">6-第0個數據列是影像的視覺效果右邊，而第0個數據行則是視覺效果上方。</span><span class="sxs-lookup"><span data-stu-id="70d6c-589">6 - The 0th row is the visual right side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="70d6c-590">7-第0個數據列是影像的視覺效果右側，而第0個數據行則是視覺效果底部。</span><span class="sxs-lookup"><span data-stu-id="70d6c-590">7 - The 0th row is the visual right side of the image, and the 0th column is the visual bottom.</span></span> <span data-ttu-id="70d6c-591">8-第0個數據列是影像左邊的視覺效果，而第0個數據行則是視覺效果底部。</span><span class="sxs-lookup"><span data-stu-id="70d6c-591">8 - The 0th row is the visual left side of the image, and the 0th column is the visual bottom.</span></span>



 

## <a name="propertytagsamplesperpixel"></a><span data-ttu-id="70d6c-592">PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="70d6c-592">PropertyTagSamplesPerPixel</span></span>

<span data-ttu-id="70d6c-593">每個圖元的色彩元件數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-593">Number of color components per pixel.</span></span>



| <span data-ttu-id="70d6c-594">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-594">Property info</span></span> | <span data-ttu-id="70d6c-595">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-595">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-596">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-596">Tag</span></span>   | <span data-ttu-id="70d6c-597">0x0115</span><span class="sxs-lookup"><span data-stu-id="70d6c-597">0x0115</span></span>               |
| <span data-ttu-id="70d6c-598">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-598">Type</span></span>  | <span data-ttu-id="70d6c-599">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-599">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-600">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-600">Count</span></span> | <span data-ttu-id="70d6c-601">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-601">1</span></span>                    |



 

## <a name="propertytagrowsperstrip"></a><span data-ttu-id="70d6c-602">PropertyTagRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="70d6c-602">PropertyTagRowsPerStrip</span></span>

<span data-ttu-id="70d6c-603">每個資料列的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-603">Number of rows per strip.</span></span> <span data-ttu-id="70d6c-604">另請參閱 [PropertyTagStripBytesCount](#propertytagstripbytescount) 和 [PropertyTagStripOffsets](#propertytagstripoffsets)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-604">See also [PropertyTagStripBytesCount](#propertytagstripbytescount) and [PropertyTagStripOffsets](#propertytagstripoffsets).</span></span>



| <span data-ttu-id="70d6c-605">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-605">Property info</span></span> | <span data-ttu-id="70d6c-606">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-606">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-607">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-607">Tag</span></span>   | <span data-ttu-id="70d6c-608">0x0116</span><span class="sxs-lookup"><span data-stu-id="70d6c-608">0x0116</span></span>                                      |
| <span data-ttu-id="70d6c-609">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-609">Type</span></span>  | <span data-ttu-id="70d6c-610">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-610">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-611">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-611">Count</span></span> | <span data-ttu-id="70d6c-612">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-612">1</span></span>                                           |



 

## <a name="propertytagstripbytescount"></a><span data-ttu-id="70d6c-613">PropertyTagStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="70d6c-613">PropertyTagStripBytesCount</span></span>

<span data-ttu-id="70d6c-614">對於每個區域，該區域中的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-614">For each strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="70d6c-615">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-615">Property info</span></span> | <span data-ttu-id="70d6c-616">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-616">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-617">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-617">Tag</span></span>   | <span data-ttu-id="70d6c-618">0x0117</span><span class="sxs-lookup"><span data-stu-id="70d6c-618">0x0117</span></span>                                      |
| <span data-ttu-id="70d6c-619">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-619">Type</span></span>  | <span data-ttu-id="70d6c-620">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-620">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-621">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-621">Count</span></span> | <span data-ttu-id="70d6c-622">停車數</span><span class="sxs-lookup"><span data-stu-id="70d6c-622">Number of strips</span></span>                            |



 

## <a name="propertytagminsamplevalue"></a><span data-ttu-id="70d6c-623">PropertyTagMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="70d6c-623">PropertyTagMinSampleValue</span></span>

<span data-ttu-id="70d6c-624">針對每個色彩元件，指派給該元件的最小值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-624">For each color component, the minimum value assigned to that component.</span></span> <span data-ttu-id="70d6c-625">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-625">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-626">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-626">Property info</span></span> | <span data-ttu-id="70d6c-627">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-627">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-628">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-628">Tag</span></span>   | <span data-ttu-id="70d6c-629">0x0118</span><span class="sxs-lookup"><span data-stu-id="70d6c-629">0x0118</span></span>                                   |
| <span data-ttu-id="70d6c-630">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-630">Type</span></span>  | <span data-ttu-id="70d6c-631">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-631">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="70d6c-632">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-632">Count</span></span> | <span data-ttu-id="70d6c-633">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-633">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagmaxsamplevalue"></a><span data-ttu-id="70d6c-634">PropertyTagMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="70d6c-634">PropertyTagMaxSampleValue</span></span>

<span data-ttu-id="70d6c-635">針對每個色彩元件，指派給該元件的最大值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-635">For each color component, the maximum value assigned to that component.</span></span> <span data-ttu-id="70d6c-636">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-636">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-637">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-637">Property info</span></span> | <span data-ttu-id="70d6c-638">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-638">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-639">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-639">Tag</span></span>   | <span data-ttu-id="70d6c-640">0x0119</span><span class="sxs-lookup"><span data-stu-id="70d6c-640">0x0119</span></span>                                   |
| <span data-ttu-id="70d6c-641">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-641">Type</span></span>  | <span data-ttu-id="70d6c-642">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-642">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="70d6c-643">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-643">Count</span></span> | <span data-ttu-id="70d6c-644">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-644">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagxresolution"></a><span data-ttu-id="70d6c-645">PropertyTagXResolution</span><span class="sxs-lookup"><span data-stu-id="70d6c-645">PropertyTagXResolution</span></span>

<span data-ttu-id="70d6c-646">影像寬度的每單位圖元數 (x) 方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-646">Number of pixels per unit in the image width (x) direction.</span></span> <span data-ttu-id="70d6c-647">單位是由 [PropertyTagResolutionUnit](#propertytagresolutionunit)所指定。</span><span class="sxs-lookup"><span data-stu-id="70d6c-647">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="70d6c-648">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-648">Property info</span></span> | <span data-ttu-id="70d6c-649">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-649">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-650">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-650">Tag</span></span>   | <span data-ttu-id="70d6c-651">0x011A</span><span class="sxs-lookup"><span data-stu-id="70d6c-651">0x011A</span></span>                  |
| <span data-ttu-id="70d6c-652">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-652">Type</span></span>  | <span data-ttu-id="70d6c-653">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-653">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-654">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-654">Count</span></span> | <span data-ttu-id="70d6c-655">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-655">1</span></span>                       |



 

## <a name="propertytagyresolution"></a><span data-ttu-id="70d6c-656">PropertyTagYResolution</span><span class="sxs-lookup"><span data-stu-id="70d6c-656">PropertyTagYResolution</span></span>

<span data-ttu-id="70d6c-657">影像高度 (y) 方向的每單位圖元數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-657">Number of pixels per unit in the image height (y) direction.</span></span> <span data-ttu-id="70d6c-658">單位是由 [PropertyTagResolutionUnit](#propertytagresolutionunit)所指定。</span><span class="sxs-lookup"><span data-stu-id="70d6c-658">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="70d6c-659">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-659">Property info</span></span> | <span data-ttu-id="70d6c-660">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-660">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-661">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-661">Tag</span></span>   | <span data-ttu-id="70d6c-662">0x011B</span><span class="sxs-lookup"><span data-stu-id="70d6c-662">0x011B</span></span>                  |
| <span data-ttu-id="70d6c-663">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-663">Type</span></span>  | <span data-ttu-id="70d6c-664">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-664">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-665">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-665">Count</span></span> | <span data-ttu-id="70d6c-666">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-666">1</span></span>                       |



 

## <a name="propertytagplanarconfig"></a><span data-ttu-id="70d6c-667">PropertyTagPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="70d6c-667">PropertyTagPlanarConfig</span></span>

<span data-ttu-id="70d6c-668">圖元元件是否以大量或平面格式記錄。</span><span class="sxs-lookup"><span data-stu-id="70d6c-668">Whether pixel components are recorded in chunky or planar format.</span></span>



| <span data-ttu-id="70d6c-669">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-669">Property info</span></span> | <span data-ttu-id="70d6c-670">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-670">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-671">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-671">Tag</span></span>   | <span data-ttu-id="70d6c-672">0x011C</span><span class="sxs-lookup"><span data-stu-id="70d6c-672">0x011C</span></span>               |
| <span data-ttu-id="70d6c-673">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-673">Type</span></span>  | <span data-ttu-id="70d6c-674">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-674">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-675">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-675">Count</span></span> | <span data-ttu-id="70d6c-676">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-676">1</span></span>                    |



 

## <a name="propertytagpagename"></a><span data-ttu-id="70d6c-677">PropertyTagPageName</span><span class="sxs-lookup"><span data-stu-id="70d6c-677">PropertyTagPageName</span></span>

<span data-ttu-id="70d6c-678">以 Null 結束的字元字串，指定掃描影像的頁面名稱。</span><span class="sxs-lookup"><span data-stu-id="70d6c-678">Null-terminated character string that specifies the name of the page from which the image was scanned.</span></span>



| <span data-ttu-id="70d6c-679">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-679">Property info</span></span> | <span data-ttu-id="70d6c-680">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-680">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-681">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-681">Tag</span></span>   | <span data-ttu-id="70d6c-682">0x011D</span><span class="sxs-lookup"><span data-stu-id="70d6c-682">0x011D</span></span>                                             |
| <span data-ttu-id="70d6c-683">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-683">Type</span></span>  | <span data-ttu-id="70d6c-684">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-684">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-685">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-685">Count</span></span> | <span data-ttu-id="70d6c-686">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-686">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagxposition"></a><span data-ttu-id="70d6c-687">PropertyTagXPosition</span><span class="sxs-lookup"><span data-stu-id="70d6c-687">PropertyTagXPosition</span></span>

<span data-ttu-id="70d6c-688">從頁面左側到影像左邊的位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-688">Offset from the left side of the page to the left side of the image.</span></span> <span data-ttu-id="70d6c-689">測量單位是由 [PropertyTagResolutionUnit](#propertytagresolutionunit)所指定。</span><span class="sxs-lookup"><span data-stu-id="70d6c-689">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="70d6c-690">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-690">Property info</span></span> | <span data-ttu-id="70d6c-691">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-691">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-692">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-692">Tag</span></span>   | <span data-ttu-id="70d6c-693">0x011E</span><span class="sxs-lookup"><span data-stu-id="70d6c-693">0x011E</span></span>                  |
| <span data-ttu-id="70d6c-694">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-694">Type</span></span>  | <span data-ttu-id="70d6c-695">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-695">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-696">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-696">Count</span></span> | <span data-ttu-id="70d6c-697">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-697">1</span></span>                       |



 

## <a name="propertytagyposition"></a><span data-ttu-id="70d6c-698">PropertyTagYPosition</span><span class="sxs-lookup"><span data-stu-id="70d6c-698">PropertyTagYPosition</span></span>

<span data-ttu-id="70d6c-699">從頁面頂端到影像頂端的位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-699">Offset from the top of the page to the top of the image.</span></span> <span data-ttu-id="70d6c-700">測量單位是由 [PropertyTagResolutionUnit](#propertytagresolutionunit)所指定。</span><span class="sxs-lookup"><span data-stu-id="70d6c-700">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="70d6c-701">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-701">Property info</span></span> | <span data-ttu-id="70d6c-702">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-702">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-703">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-703">Tag</span></span>   | <span data-ttu-id="70d6c-704">0x011F</span><span class="sxs-lookup"><span data-stu-id="70d6c-704">0x011F</span></span>                  |
| <span data-ttu-id="70d6c-705">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-705">Type</span></span>  | <span data-ttu-id="70d6c-706">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-706">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-707">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-707">Count</span></span> | <span data-ttu-id="70d6c-708">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-708">1</span></span>                       |



 

## <a name="propertytagfreeoffset"></a><span data-ttu-id="70d6c-709">PropertyTagFreeOffset</span><span class="sxs-lookup"><span data-stu-id="70d6c-709">PropertyTagFreeOffset</span></span>

<span data-ttu-id="70d6c-710">針對連續未使用位元組的每個字串，該字串的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-710">For each string of contiguous unused bytes, the byte offset of that string.</span></span>



| <span data-ttu-id="70d6c-711">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-711">Property info</span></span> | <span data-ttu-id="70d6c-712">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-712">Value</span></span> |
|------|---------------------|
| <span data-ttu-id="70d6c-713">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-713">Tag</span></span>  | <span data-ttu-id="70d6c-714">0x0120</span><span class="sxs-lookup"><span data-stu-id="70d6c-714">0x0120</span></span>              |
| <span data-ttu-id="70d6c-715">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-715">Type</span></span> | <span data-ttu-id="70d6c-716">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-716">PropertyTagTypeLong</span></span> |



 

## <a name="propertytagfreebytecounts"></a><span data-ttu-id="70d6c-717">PropertyTagFreeByteCounts</span><span class="sxs-lookup"><span data-stu-id="70d6c-717">PropertyTagFreeByteCounts</span></span>

<span data-ttu-id="70d6c-718">針對連續未使用位元組的每個字串，該字串中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-718">For each string of contiguous unused bytes, the number of bytes in that string.</span></span>



| <span data-ttu-id="70d6c-719">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-719">Property info</span></span> | <span data-ttu-id="70d6c-720">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-720">Value</span></span> |
|-------|-----------------------------------------------|
| <span data-ttu-id="70d6c-721">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-721">Tag</span></span>   | <span data-ttu-id="70d6c-722">0x0121</span><span class="sxs-lookup"><span data-stu-id="70d6c-722">0x0121</span></span>                                        |
| <span data-ttu-id="70d6c-723">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-723">Type</span></span>  | <span data-ttu-id="70d6c-724">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-724">PropertyTagTypeLong</span></span>                           |
| <span data-ttu-id="70d6c-725">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-725">Count</span></span> | <span data-ttu-id="70d6c-726">連續未使用位元組的字串數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-726">Number of strings of contiguous unused bytes.</span></span> |



 

## <a name="propertytaggrayresponseunit"></a><span data-ttu-id="70d6c-727">PropertyTagGrayResponseUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-727">PropertyTagGrayResponseUnit</span></span>

<span data-ttu-id="70d6c-728">PropertyTagGrayResponseCurve 所指定之數位的精確度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-728">Precision of the number specified by PropertyTagGrayResponseCurve.</span></span> <span data-ttu-id="70d6c-729">1指定十分之一、2指定百分之一、3指定千位等。</span><span class="sxs-lookup"><span data-stu-id="70d6c-729">1 specifies tenths, 2 specifies hundredths, 3 specifies thousandths, and so on.</span></span>



| <span data-ttu-id="70d6c-730">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-730">Property info</span></span> | <span data-ttu-id="70d6c-731">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-731">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-732">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-732">Tag</span></span>   | <span data-ttu-id="70d6c-733">0x0122</span><span class="sxs-lookup"><span data-stu-id="70d6c-733">0x0122</span></span>               |
| <span data-ttu-id="70d6c-734">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-734">Type</span></span>  | <span data-ttu-id="70d6c-735">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-735">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-736">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-736">Count</span></span> | <span data-ttu-id="70d6c-737">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-737">1</span></span>                    |



 

## <a name="propertytaggrayresponsecurve"></a><span data-ttu-id="70d6c-738">PropertyTagGrayResponseCurve</span><span class="sxs-lookup"><span data-stu-id="70d6c-738">PropertyTagGrayResponseCurve</span></span>

<span data-ttu-id="70d6c-739">針對灰階影像中的每個可能圖元值，這是該圖元值的光學密度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-739">For each possible pixel value in a grayscale image, the optical density of that pixel value.</span></span>



| <span data-ttu-id="70d6c-740">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-740">Property info</span></span> | <span data-ttu-id="70d6c-741">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-741">Value</span></span> |
|-------|---------------------------------|
| <span data-ttu-id="70d6c-742">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-742">Tag</span></span>   | <span data-ttu-id="70d6c-743">0x0123</span><span class="sxs-lookup"><span data-stu-id="70d6c-743">0x0123</span></span>                          |
| <span data-ttu-id="70d6c-744">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-744">Type</span></span>  | <span data-ttu-id="70d6c-745">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-745">PropertyTagTypeShort</span></span>            |
| <span data-ttu-id="70d6c-746">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-746">Count</span></span> | <span data-ttu-id="70d6c-747">可能圖元值的數目</span><span class="sxs-lookup"><span data-stu-id="70d6c-747">Number of possible pixel values</span></span> |



 

## <a name="propertytagt4option"></a><span data-ttu-id="70d6c-748">PropertyTagT4Option</span><span class="sxs-lookup"><span data-stu-id="70d6c-748">PropertyTagT4Option</span></span>

<span data-ttu-id="70d6c-749">與 T4 編碼相關的一組旗標。</span><span class="sxs-lookup"><span data-stu-id="70d6c-749">Set of flags that relate to T4 encoding.</span></span>



| <span data-ttu-id="70d6c-750">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-750">Property info</span></span> | <span data-ttu-id="70d6c-751">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-751">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-752">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-752">Tag</span></span>   | <span data-ttu-id="70d6c-753">0x0124</span><span class="sxs-lookup"><span data-stu-id="70d6c-753">0x0124</span></span>              |
| <span data-ttu-id="70d6c-754">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-754">Type</span></span>  | <span data-ttu-id="70d6c-755">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-755">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-756">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-756">Count</span></span> | <span data-ttu-id="70d6c-757">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-757">1</span></span>                   |



 

## <a name="propertytagt6option"></a><span data-ttu-id="70d6c-758">PropertyTagT6Option</span><span class="sxs-lookup"><span data-stu-id="70d6c-758">PropertyTagT6Option</span></span>

<span data-ttu-id="70d6c-759">與 T6 編碼相關的旗標集合。</span><span class="sxs-lookup"><span data-stu-id="70d6c-759">Set of flags that relate to T6 encoding.</span></span>



| <span data-ttu-id="70d6c-760">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-760">Property info</span></span> | <span data-ttu-id="70d6c-761">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-761">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-762">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-762">Tag</span></span>   | <span data-ttu-id="70d6c-763">0x0125</span><span class="sxs-lookup"><span data-stu-id="70d6c-763">0x0125</span></span>              |
| <span data-ttu-id="70d6c-764">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-764">Type</span></span>  | <span data-ttu-id="70d6c-765">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-765">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-766">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-766">Count</span></span> | <span data-ttu-id="70d6c-767">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-767">1</span></span>                   |



 

## <a name="propertytagresolutionunit"></a><span data-ttu-id="70d6c-768">PropertyTagResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-768">PropertyTagResolutionUnit</span></span>

<span data-ttu-id="70d6c-769">水準解析度和垂直解析度的測量單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-769">Unit of measure for the horizontal resolution and the vertical resolution.</span></span>



<span data-ttu-id="70d6c-770">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-770">Tag</span></span>

<span data-ttu-id="70d6c-771">0x0128</span><span class="sxs-lookup"><span data-stu-id="70d6c-771">0x0128</span></span>

<span data-ttu-id="70d6c-772">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-772">Type</span></span>

<span data-ttu-id="70d6c-773">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-773">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-774">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-774">Count</span></span>

<span data-ttu-id="70d6c-775">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-775">1</span></span>

<span data-ttu-id="70d6c-776">2-英寸 3-釐米</span><span class="sxs-lookup"><span data-stu-id="70d6c-776">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagpagenumber"></a><span data-ttu-id="70d6c-777">PropertyTagPageNumber</span><span class="sxs-lookup"><span data-stu-id="70d6c-777">PropertyTagPageNumber</span></span>

<span data-ttu-id="70d6c-778">掃描影像的頁面頁碼。</span><span class="sxs-lookup"><span data-stu-id="70d6c-778">Page number of the page from which the image was scanned.</span></span>



| <span data-ttu-id="70d6c-779">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-779">Property info</span></span> | <span data-ttu-id="70d6c-780">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-780">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-781">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-781">Tag</span></span>   | <span data-ttu-id="70d6c-782">0x0129</span><span class="sxs-lookup"><span data-stu-id="70d6c-782">0x0129</span></span>               |
| <span data-ttu-id="70d6c-783">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-783">Type</span></span>  | <span data-ttu-id="70d6c-784">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-784">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-785">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-785">Count</span></span> | <span data-ttu-id="70d6c-786">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-786">1</span></span>                    |



 

## <a name="propertytagtransferfunction"></a><span data-ttu-id="70d6c-787">PropertyTagTransferFunction</span><span class="sxs-lookup"><span data-stu-id="70d6c-787">PropertyTagTransferFunction</span></span>

<span data-ttu-id="70d6c-788">為影像指定傳送函數的資料表。</span><span class="sxs-lookup"><span data-stu-id="70d6c-788">Tables that specify transfer functions for the image.</span></span>



| <span data-ttu-id="70d6c-789">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-789">Property info</span></span> | <span data-ttu-id="70d6c-790">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-790">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="70d6c-791">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-791">Tag</span></span>   | <span data-ttu-id="70d6c-792">0x012D</span><span class="sxs-lookup"><span data-stu-id="70d6c-792">0x012D</span></span>                                               |
| <span data-ttu-id="70d6c-793">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-793">Type</span></span>  | <span data-ttu-id="70d6c-794">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-794">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="70d6c-795">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-795">Count</span></span> | <span data-ttu-id="70d6c-796">資料表所需的16位單字總數</span><span class="sxs-lookup"><span data-stu-id="70d6c-796">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagsoftwareused"></a><span data-ttu-id="70d6c-797">PropertyTagSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="70d6c-797">PropertyTagSoftwareUsed</span></span>

<span data-ttu-id="70d6c-798">以 Null 結束的字元字串，指定用來產生映射之裝置的軟體或固件的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="70d6c-798">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the image.</span></span>



| <span data-ttu-id="70d6c-799">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-799">Property info</span></span> | <span data-ttu-id="70d6c-800">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-800">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-801">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-801">Tag</span></span>   | <span data-ttu-id="70d6c-802">0x0131</span><span class="sxs-lookup"><span data-stu-id="70d6c-802">0x0131</span></span>                                             |
| <span data-ttu-id="70d6c-803">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-803">Type</span></span>  | <span data-ttu-id="70d6c-804">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-804">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-805">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-805">Count</span></span> | <span data-ttu-id="70d6c-806">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-806">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagdatetime"></a><span data-ttu-id="70d6c-807">PropertyTagDateTime</span><span class="sxs-lookup"><span data-stu-id="70d6c-807">PropertyTagDateTime</span></span>

<span data-ttu-id="70d6c-808">建立映射的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="70d6c-808">Date and time the image was created.</span></span>



| <span data-ttu-id="70d6c-809">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-809">Property info</span></span> | <span data-ttu-id="70d6c-810">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-810">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-811">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-811">Tag</span></span>   | <span data-ttu-id="70d6c-812">0x0132</span><span class="sxs-lookup"><span data-stu-id="70d6c-812">0x0132</span></span>               |
| <span data-ttu-id="70d6c-813">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-813">Type</span></span>  | <span data-ttu-id="70d6c-814">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-814">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="70d6c-815">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-815">Count</span></span> | <span data-ttu-id="70d6c-816">20</span><span class="sxs-lookup"><span data-stu-id="70d6c-816">20</span></span>                   |



 

## <a name="propertytagartist"></a><span data-ttu-id="70d6c-817">PropertyTagArtist</span><span class="sxs-lookup"><span data-stu-id="70d6c-817">PropertyTagArtist</span></span>

<span data-ttu-id="70d6c-818">以 Null 結束的字元字串，指定建立影像的人員名稱。</span><span class="sxs-lookup"><span data-stu-id="70d6c-818">Null-terminated character string that specifies the name of the person who created the image.</span></span>



| <span data-ttu-id="70d6c-819">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-819">Property info</span></span> | <span data-ttu-id="70d6c-820">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-820">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-821">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-821">Tag</span></span>   | <span data-ttu-id="70d6c-822">0x013B</span><span class="sxs-lookup"><span data-stu-id="70d6c-822">0x013B</span></span>                                             |
| <span data-ttu-id="70d6c-823">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-823">Type</span></span>  | <span data-ttu-id="70d6c-824">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-824">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-825">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-825">Count</span></span> | <span data-ttu-id="70d6c-826">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-826">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaghostcomputer"></a><span data-ttu-id="70d6c-827">PropertyTagHostComputer</span><span class="sxs-lookup"><span data-stu-id="70d6c-827">PropertyTagHostComputer</span></span>

<span data-ttu-id="70d6c-828">以 Null 結束的字元字串，指定用來建立映射的電腦和/或作業系統。</span><span class="sxs-lookup"><span data-stu-id="70d6c-828">Null-terminated character string that specifies the computer and/or operating system used to create the image.</span></span>



| <span data-ttu-id="70d6c-829">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-829">Property info</span></span> | <span data-ttu-id="70d6c-830">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-830">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-831">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-831">Tag</span></span>   | <span data-ttu-id="70d6c-832">0x013C</span><span class="sxs-lookup"><span data-stu-id="70d6c-832">0x013C</span></span>                                             |
| <span data-ttu-id="70d6c-833">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-833">Type</span></span>  | <span data-ttu-id="70d6c-834">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-834">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-835">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-835">Count</span></span> | <span data-ttu-id="70d6c-836">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-836">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagpredictor"></a><span data-ttu-id="70d6c-837">PropertyTagPredictor</span><span class="sxs-lookup"><span data-stu-id="70d6c-837">PropertyTagPredictor</span></span>

<span data-ttu-id="70d6c-838">套用編碼配置之前，套用至影像資料的預測配置類型。</span><span class="sxs-lookup"><span data-stu-id="70d6c-838">Type of prediction scheme that was applied to the image data before the encoding scheme was applied.</span></span>



| <span data-ttu-id="70d6c-839">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-839">Property info</span></span> | <span data-ttu-id="70d6c-840">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-840">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-841">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-841">Tag</span></span>   | <span data-ttu-id="70d6c-842">0x013D</span><span class="sxs-lookup"><span data-stu-id="70d6c-842">0x013D</span></span>               |
| <span data-ttu-id="70d6c-843">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-843">Type</span></span>  | <span data-ttu-id="70d6c-844">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-844">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-845">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-845">Count</span></span> | <span data-ttu-id="70d6c-846">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-846">1</span></span>                    |



 

## <a name="propertytagwhitepoint"></a><span data-ttu-id="70d6c-847">PropertyTagWhitePoint</span><span class="sxs-lookup"><span data-stu-id="70d6c-847">PropertyTagWhitePoint</span></span>

<span data-ttu-id="70d6c-848">影像的白色點 Chromaticity。</span><span class="sxs-lookup"><span data-stu-id="70d6c-848">Chromaticity of the white point of the image.</span></span>



| <span data-ttu-id="70d6c-849">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-849">Property info</span></span> | <span data-ttu-id="70d6c-850">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-850">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-851">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-851">Tag</span></span>   | <span data-ttu-id="70d6c-852">0x013E</span><span class="sxs-lookup"><span data-stu-id="70d6c-852">0x013E</span></span>                  |
| <span data-ttu-id="70d6c-853">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-853">Type</span></span>  | <span data-ttu-id="70d6c-854">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-854">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-855">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-855">Count</span></span> | <span data-ttu-id="70d6c-856">2</span><span class="sxs-lookup"><span data-stu-id="70d6c-856">2</span></span>                       |



 

## <a name="propertytagprimarychromaticities"></a><span data-ttu-id="70d6c-857">PropertyTagPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="70d6c-857">PropertyTagPrimaryChromaticities</span></span>

<span data-ttu-id="70d6c-858">針對影像中的三種主要色彩，這是該色彩的 chromaticity。</span><span class="sxs-lookup"><span data-stu-id="70d6c-858">For each of the three primary colors in the image, the chromaticity of that color.</span></span>



| <span data-ttu-id="70d6c-859">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-859">Property info</span></span> | <span data-ttu-id="70d6c-860">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-860">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-861">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-861">Tag</span></span>   | <span data-ttu-id="70d6c-862">0x013F</span><span class="sxs-lookup"><span data-stu-id="70d6c-862">0x013F</span></span>                  |
| <span data-ttu-id="70d6c-863">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-863">Type</span></span>  | <span data-ttu-id="70d6c-864">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-864">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-865">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-865">Count</span></span> | <span data-ttu-id="70d6c-866">6</span><span class="sxs-lookup"><span data-stu-id="70d6c-866">6</span></span>                       |



 

## <a name="propertytagcolormap"></a><span data-ttu-id="70d6c-867">PropertyTagColorMap</span><span class="sxs-lookup"><span data-stu-id="70d6c-867">PropertyTagColorMap</span></span>

<span data-ttu-id="70d6c-868">調色板索引影像的色調色板 (查閱資料表) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-868">Color palette (lookup table) for a palette-indexed image.</span></span>



| <span data-ttu-id="70d6c-869">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-869">Property info</span></span> | <span data-ttu-id="70d6c-870">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-870">Value</span></span> |
|-------|-------------------------------------------------|
| <span data-ttu-id="70d6c-871">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-871">Tag</span></span>   | <span data-ttu-id="70d6c-872">0x0140</span><span class="sxs-lookup"><span data-stu-id="70d6c-872">0x0140</span></span>                                          |
| <span data-ttu-id="70d6c-873">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-873">Type</span></span>  | <span data-ttu-id="70d6c-874">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-874">PropertyTagTypeShort</span></span>                            |
| <span data-ttu-id="70d6c-875">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-875">Count</span></span> | <span data-ttu-id="70d6c-876">調色板所需的16位字組數目</span><span class="sxs-lookup"><span data-stu-id="70d6c-876">Number of 16-bit words required for the palette</span></span> |



 

## <a name="propertytaghalftonehints"></a><span data-ttu-id="70d6c-877">PropertyTagHalftoneHints</span><span class="sxs-lookup"><span data-stu-id="70d6c-877">PropertyTagHalftoneHints</span></span>

<span data-ttu-id="70d6c-878">半色調函數所使用的資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-878">Information used by the halftone function</span></span>



| <span data-ttu-id="70d6c-879">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-879">Property info</span></span> | <span data-ttu-id="70d6c-880">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-880">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-881">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-881">Tag</span></span>   | <span data-ttu-id="70d6c-882">0x0141</span><span class="sxs-lookup"><span data-stu-id="70d6c-882">0x0141</span></span>               |
| <span data-ttu-id="70d6c-883">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-883">Type</span></span>  | <span data-ttu-id="70d6c-884">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-884">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-885">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-885">Count</span></span> | <span data-ttu-id="70d6c-886">2</span><span class="sxs-lookup"><span data-stu-id="70d6c-886">2</span></span>                    |



 

## <a name="propertytagtilewidth"></a><span data-ttu-id="70d6c-887">PropertyTagTileWidth</span><span class="sxs-lookup"><span data-stu-id="70d6c-887">PropertyTagTileWidth</span></span>

<span data-ttu-id="70d6c-888">每個圖格中的圖元資料行數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-888">Number of pixel columns in each tile.</span></span>



| <span data-ttu-id="70d6c-889">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-889">Property info</span></span> | <span data-ttu-id="70d6c-890">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-890">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-891">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-891">Tag</span></span>   | <span data-ttu-id="70d6c-892">0x0142</span><span class="sxs-lookup"><span data-stu-id="70d6c-892">0x0142</span></span>                                      |
| <span data-ttu-id="70d6c-893">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-893">Type</span></span>  | <span data-ttu-id="70d6c-894">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-894">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-895">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-895">Count</span></span> | <span data-ttu-id="70d6c-896">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-896">1</span></span>                                           |



 

## <a name="propertytagtilelength"></a><span data-ttu-id="70d6c-897">PropertyTagTileLength</span><span class="sxs-lookup"><span data-stu-id="70d6c-897">PropertyTagTileLength</span></span>

<span data-ttu-id="70d6c-898">每個圖格中的圖元資料列數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-898">Number of pixel rows in each tile.</span></span>



| <span data-ttu-id="70d6c-899">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-899">Property info</span></span> | <span data-ttu-id="70d6c-900">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-900">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-901">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-901">Tag</span></span>   | <span data-ttu-id="70d6c-902">0x0143</span><span class="sxs-lookup"><span data-stu-id="70d6c-902">0x0143</span></span>                                      |
| <span data-ttu-id="70d6c-903">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-903">Type</span></span>  | <span data-ttu-id="70d6c-904">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-904">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-905">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-905">Count</span></span> | <span data-ttu-id="70d6c-906">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-906">1</span></span>                                           |



 

## <a name="propertytagtileoffset"></a><span data-ttu-id="70d6c-907">PropertyTagTileOffset</span><span class="sxs-lookup"><span data-stu-id="70d6c-907">PropertyTagTileOffset</span></span>

<span data-ttu-id="70d6c-908">針對每個磚，即該磚的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-908">For each tile, the byte offset of that tile.</span></span>



| <span data-ttu-id="70d6c-909">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-909">Property info</span></span> | <span data-ttu-id="70d6c-910">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-910">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-911">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-911">Tag</span></span>   | <span data-ttu-id="70d6c-912">0x0144</span><span class="sxs-lookup"><span data-stu-id="70d6c-912">0x0144</span></span>              |
| <span data-ttu-id="70d6c-913">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-913">Type</span></span>  | <span data-ttu-id="70d6c-914">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-914">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-915">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-915">Count</span></span> | <span data-ttu-id="70d6c-916">磚數目</span><span class="sxs-lookup"><span data-stu-id="70d6c-916">Number of tiles</span></span>     |



 

## <a name="propertytagtilebytecounts"></a><span data-ttu-id="70d6c-917">PropertyTagTileByteCounts</span><span class="sxs-lookup"><span data-stu-id="70d6c-917">PropertyTagTileByteCounts</span></span>

<span data-ttu-id="70d6c-918">針對每個磚，即該磚中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-918">For each tile, the number of bytes in that tile.</span></span>



| <span data-ttu-id="70d6c-919">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-919">Property info</span></span> | <span data-ttu-id="70d6c-920">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-920">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-921">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-921">Tag</span></span>   | <span data-ttu-id="70d6c-922">0x0145</span><span class="sxs-lookup"><span data-stu-id="70d6c-922">0x0145</span></span>                                      |
| <span data-ttu-id="70d6c-923">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-923">Type</span></span>  | <span data-ttu-id="70d6c-924">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-924">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-925">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-925">Count</span></span> | <span data-ttu-id="70d6c-926">磚數目</span><span class="sxs-lookup"><span data-stu-id="70d6c-926">Number of tiles</span></span>                             |



 

## <a name="propertytaginkset"></a><span data-ttu-id="70d6c-927">PropertyTagInkSet</span><span class="sxs-lookup"><span data-stu-id="70d6c-927">PropertyTagInkSet</span></span>

<span data-ttu-id="70d6c-928">用於分隔影像中的一組墨水。</span><span class="sxs-lookup"><span data-stu-id="70d6c-928">Set of inks used in a separated image.</span></span>



| <span data-ttu-id="70d6c-929">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-929">Property info</span></span> | <span data-ttu-id="70d6c-930">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-930">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-931">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-931">Tag</span></span>   | <span data-ttu-id="70d6c-932">0x014C</span><span class="sxs-lookup"><span data-stu-id="70d6c-932">0x014C</span></span>               |
| <span data-ttu-id="70d6c-933">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-933">Type</span></span>  | <span data-ttu-id="70d6c-934">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-934">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-935">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-935">Count</span></span> | <span data-ttu-id="70d6c-936">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-936">1</span></span>                    |



 

## <a name="propertytaginknames"></a><span data-ttu-id="70d6c-937">PropertyTagInkNames</span><span class="sxs-lookup"><span data-stu-id="70d6c-937">PropertyTagInkNames</span></span>

<span data-ttu-id="70d6c-938">串連、以 null 結束的字元字串順序，指定用於分隔影像中的油墨名稱。</span><span class="sxs-lookup"><span data-stu-id="70d6c-938">Sequence of concatenated, null-terminated, character strings that specify the names of the inks used in a separated image.</span></span>



| <span data-ttu-id="70d6c-939">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-939">Property info</span></span> | <span data-ttu-id="70d6c-940">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-940">Value</span></span> |
|-------|------------------------------------------------------------------------|
| <span data-ttu-id="70d6c-941">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-941">Tag</span></span>   | <span data-ttu-id="70d6c-942">0x014D</span><span class="sxs-lookup"><span data-stu-id="70d6c-942">0x014D</span></span>                                                                 |
| <span data-ttu-id="70d6c-943">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-943">Type</span></span>  | <span data-ttu-id="70d6c-944">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-944">PropertyTagTypeASCII</span></span>                                                   |
| <span data-ttu-id="70d6c-945">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-945">Count</span></span> | <span data-ttu-id="70d6c-946">字串序列的總長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-946">Total length of the sequence of strings including the NULL terminators</span></span> |



 

## <a name="propertytagnumberofinks"></a><span data-ttu-id="70d6c-947">PropertyTagNumberOfInks</span><span class="sxs-lookup"><span data-stu-id="70d6c-947">PropertyTagNumberOfInks</span></span>

<span data-ttu-id="70d6c-948">油墨數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-948">Number of inks.</span></span>



| <span data-ttu-id="70d6c-949">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-949">Property info</span></span> | <span data-ttu-id="70d6c-950">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-950">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-951">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-951">Tag</span></span>   | <span data-ttu-id="70d6c-952">0x014E</span><span class="sxs-lookup"><span data-stu-id="70d6c-952">0x014E</span></span>               |
| <span data-ttu-id="70d6c-953">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-953">Type</span></span>  | <span data-ttu-id="70d6c-954">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-954">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-955">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-955">Count</span></span> | <span data-ttu-id="70d6c-956">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-956">1</span></span>                    |



 

## <a name="propertytagdotrange"></a><span data-ttu-id="70d6c-957">PropertyTagDotRange</span><span class="sxs-lookup"><span data-stu-id="70d6c-957">PropertyTagDotRange</span></span>

<span data-ttu-id="70d6c-958">對應至0% 點和100% 點的色彩元件值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-958">Color component values that correspond to a 0 percent dot and a 100 percent dot.</span></span>



| <span data-ttu-id="70d6c-959">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-959">Property info</span></span> | <span data-ttu-id="70d6c-960">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-960">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-961">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-961">Tag</span></span>   | <span data-ttu-id="70d6c-962">0x0150</span><span class="sxs-lookup"><span data-stu-id="70d6c-962">0x0150</span></span>                                      |
| <span data-ttu-id="70d6c-963">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-963">Type</span></span>  | <span data-ttu-id="70d6c-964">PropertyTagTypeByte 或 PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-964">PropertyTagTypeByte or PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-965">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-965">Count</span></span> | <span data-ttu-id="70d6c-966">2或2× PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="70d6c-966">2 or 2×PropertyTagSamplesPerPixel</span></span>           |



 

## <a name="propertytagtargetprinter"></a><span data-ttu-id="70d6c-967">PropertyTagTargetPrinter</span><span class="sxs-lookup"><span data-stu-id="70d6c-967">PropertyTagTargetPrinter</span></span>

<span data-ttu-id="70d6c-968">以 Null 結束的字元字串，描述預期的列印環境。</span><span class="sxs-lookup"><span data-stu-id="70d6c-968">Null-terminated character string that describes the intended printing environment.</span></span>



| <span data-ttu-id="70d6c-969">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-969">Property info</span></span> | <span data-ttu-id="70d6c-970">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-970">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-971">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-971">Tag</span></span>   | <span data-ttu-id="70d6c-972">0x0151</span><span class="sxs-lookup"><span data-stu-id="70d6c-972">0x0151</span></span>                                             |
| <span data-ttu-id="70d6c-973">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-973">Type</span></span>  | <span data-ttu-id="70d6c-974">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-974">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-975">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-975">Count</span></span> | <span data-ttu-id="70d6c-976">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-976">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagextrasamples"></a><span data-ttu-id="70d6c-977">PropertyTagExtraSamples</span><span class="sxs-lookup"><span data-stu-id="70d6c-977">PropertyTagExtraSamples</span></span>

<span data-ttu-id="70d6c-978">額外色彩元件的數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-978">Number of extra color components.</span></span> <span data-ttu-id="70d6c-979">例如，一個額外的元件可能會保存 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-979">For example, one extra component might hold an alpha value.</span></span>



| <span data-ttu-id="70d6c-980">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-980">Property info</span></span> | <span data-ttu-id="70d6c-981">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-981">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-982">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-982">Tag</span></span>   | <span data-ttu-id="70d6c-983">0x0152</span><span class="sxs-lookup"><span data-stu-id="70d6c-983">0x0152</span></span>               |
| <span data-ttu-id="70d6c-984">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-984">Type</span></span>  | <span data-ttu-id="70d6c-985">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-985">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-986">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-986">Count</span></span> | <span data-ttu-id="70d6c-987">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-987">1</span></span>                    |



 

## <a name="propertytagsampleformat"></a><span data-ttu-id="70d6c-988">PropertyTagSampleFormat</span><span class="sxs-lookup"><span data-stu-id="70d6c-988">PropertyTagSampleFormat</span></span>

<span data-ttu-id="70d6c-989">針對每個色彩元件，數值格式 (該元件的未簽署、帶正負號、浮點數) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-989">For each color component, the numerical format (unsigned, signed, floating point) of that component.</span></span> <span data-ttu-id="70d6c-990">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-990">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-991">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-991">Property info</span></span> | <span data-ttu-id="70d6c-992">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-992">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-993">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-993">Tag</span></span>   | <span data-ttu-id="70d6c-994">0x0153</span><span class="sxs-lookup"><span data-stu-id="70d6c-994">0x0153</span></span>                                   |
| <span data-ttu-id="70d6c-995">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-995">Type</span></span>  | <span data-ttu-id="70d6c-996">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-996">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="70d6c-997">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-997">Count</span></span> | <span data-ttu-id="70d6c-998">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-998">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagsminsamplevalue"></a><span data-ttu-id="70d6c-999">PropertyTagSMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="70d6c-999">PropertyTagSMinSampleValue</span></span>

<span data-ttu-id="70d6c-1000">針對每個色彩元件，該元件的最小值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1000">For each color component, the minimum value of that component.</span></span> <span data-ttu-id="70d6c-1001">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1001">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-1002">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1002">Property info</span></span> | <span data-ttu-id="70d6c-1003">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1003">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="70d6c-1004">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1004">Tag</span></span>   | <span data-ttu-id="70d6c-1005">0x0154</span><span class="sxs-lookup"><span data-stu-id="70d6c-1005">0x0154</span></span>                                              |
| <span data-ttu-id="70d6c-1006">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1006">Type</span></span>  | <span data-ttu-id="70d6c-1007">最符合圖元元件資料的類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1007">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="70d6c-1008">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1008">Count</span></span> | <span data-ttu-id="70d6c-1009">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1009">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagsmaxsamplevalue"></a><span data-ttu-id="70d6c-1010">PropertyTagSMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="70d6c-1010">PropertyTagSMaxSampleValue</span></span>

<span data-ttu-id="70d6c-1011">針對每個色彩元件，該元件的最大值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1011">For each color component, the maximum value of that component.</span></span> <span data-ttu-id="70d6c-1012">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1012">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-1013">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1013">Property info</span></span> | <span data-ttu-id="70d6c-1014">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1014">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="70d6c-1015">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1015">Tag</span></span>   | <span data-ttu-id="70d6c-1016">0x0155</span><span class="sxs-lookup"><span data-stu-id="70d6c-1016">0x0155</span></span>                                              |
| <span data-ttu-id="70d6c-1017">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1017">Type</span></span>  | <span data-ttu-id="70d6c-1018">最符合圖元元件資料的類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1018">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="70d6c-1019">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1019">Count</span></span> | <span data-ttu-id="70d6c-1020">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1020">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagtransferrange"></a><span data-ttu-id="70d6c-1021">PropertyTagTransferRange</span><span class="sxs-lookup"><span data-stu-id="70d6c-1021">PropertyTagTransferRange</span></span>

<span data-ttu-id="70d6c-1022">擴充傳送函數範圍之值的資料表。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1022">Table of values that extends the range of the transfer function.</span></span>



| <span data-ttu-id="70d6c-1023">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1023">Property info</span></span> | <span data-ttu-id="70d6c-1024">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1024">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1025">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1025">Tag</span></span>   | <span data-ttu-id="70d6c-1026">0x0156</span><span class="sxs-lookup"><span data-stu-id="70d6c-1026">0x0156</span></span>               |
| <span data-ttu-id="70d6c-1027">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1027">Type</span></span>  | <span data-ttu-id="70d6c-1028">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1028">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1029">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1029">Count</span></span> | <span data-ttu-id="70d6c-1030">6</span><span class="sxs-lookup"><span data-stu-id="70d6c-1030">6</span></span>                    |



 

## <a name="propertytagjpegproc"></a><span data-ttu-id="70d6c-1031">PropertyTagJPEGProc</span><span class="sxs-lookup"><span data-stu-id="70d6c-1031">PropertyTagJPEGProc</span></span>

<span data-ttu-id="70d6c-1032">JPEG 壓縮進程。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1032">JPEG compression process.</span></span>



| <span data-ttu-id="70d6c-1033">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1033">Property info</span></span> | <span data-ttu-id="70d6c-1034">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1034">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1035">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1035">Tag</span></span>   | <span data-ttu-id="70d6c-1036">0x0200</span><span class="sxs-lookup"><span data-stu-id="70d6c-1036">0x0200</span></span>               |
| <span data-ttu-id="70d6c-1037">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1037">Type</span></span>  | <span data-ttu-id="70d6c-1038">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1038">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1039">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1039">Count</span></span> | <span data-ttu-id="70d6c-1040">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1040">1</span></span>                    |



 

## <a name="propertytagjpeginterformat"></a><span data-ttu-id="70d6c-1041">PropertyTagJPEGInterFormat</span><span class="sxs-lookup"><span data-stu-id="70d6c-1041">PropertyTagJPEGInterFormat</span></span>

<span data-ttu-id="70d6c-1042">JPEG 位流開頭的位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1042">Offset to the start of a JPEG bitstream.</span></span>



| <span data-ttu-id="70d6c-1043">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1043">Property info</span></span> | <span data-ttu-id="70d6c-1044">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1044">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1045">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1045">Tag</span></span>   | <span data-ttu-id="70d6c-1046">0x0201</span><span class="sxs-lookup"><span data-stu-id="70d6c-1046">0x0201</span></span>              |
| <span data-ttu-id="70d6c-1047">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1047">Type</span></span>  | <span data-ttu-id="70d6c-1048">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1048">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1049">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1049">Count</span></span> | <span data-ttu-id="70d6c-1050">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1050">1</span></span>                   |



 

## <a name="propertytagjpeginterlength"></a><span data-ttu-id="70d6c-1051">PropertyTagJPEGInterLength</span><span class="sxs-lookup"><span data-stu-id="70d6c-1051">PropertyTagJPEGInterLength</span></span>

<span data-ttu-id="70d6c-1052">JPEG 位流的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1052">Length, in bytes, of the JPEG bitstream.</span></span>



| <span data-ttu-id="70d6c-1053">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1053">Property info</span></span> | <span data-ttu-id="70d6c-1054">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1054">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1055">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1055">Tag</span></span>   | <span data-ttu-id="70d6c-1056">0x0202</span><span class="sxs-lookup"><span data-stu-id="70d6c-1056">0x0202</span></span>              |
| <span data-ttu-id="70d6c-1057">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1057">Type</span></span>  | <span data-ttu-id="70d6c-1058">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1058">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1059">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1059">Count</span></span> | <span data-ttu-id="70d6c-1060">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1060">1</span></span>                   |



 

## <a name="propertytagjpegrestartinterval"></a><span data-ttu-id="70d6c-1061">PropertyTagJPEGRestartInterval</span><span class="sxs-lookup"><span data-stu-id="70d6c-1061">PropertyTagJPEGRestartInterval</span></span>

<span data-ttu-id="70d6c-1062">重新開機間隔的長度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1062">Length of the restart interval.</span></span>



| <span data-ttu-id="70d6c-1063">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1063">Property info</span></span> | <span data-ttu-id="70d6c-1064">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1064">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1065">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1065">Tag</span></span>   | <span data-ttu-id="70d6c-1066">0x0203</span><span class="sxs-lookup"><span data-stu-id="70d6c-1066">0x0203</span></span>               |
| <span data-ttu-id="70d6c-1067">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1067">Type</span></span>  | <span data-ttu-id="70d6c-1068">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1068">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1069">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1069">Count</span></span> | <span data-ttu-id="70d6c-1070">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1070">1</span></span>                    |



 

## <a name="propertytagjpeglosslesspredictors"></a><span data-ttu-id="70d6c-1071">PropertyTagJPEGLosslessPredictors</span><span class="sxs-lookup"><span data-stu-id="70d6c-1071">PropertyTagJPEGLosslessPredictors</span></span>

<span data-ttu-id="70d6c-1072">針對每個色彩元件，該元件會有不失真的預測器選取值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1072">For each color component, a lossless predictor-selection value for that component.</span></span> <span data-ttu-id="70d6c-1073">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1073">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-1074">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1074">Property info</span></span> | <span data-ttu-id="70d6c-1075">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1075">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-1076">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1076">Tag</span></span>   | <span data-ttu-id="70d6c-1077">0x0205</span><span class="sxs-lookup"><span data-stu-id="70d6c-1077">0x0205</span></span>                                   |
| <span data-ttu-id="70d6c-1078">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1078">Type</span></span>  | <span data-ttu-id="70d6c-1079">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1079">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="70d6c-1080">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1080">Count</span></span> | <span data-ttu-id="70d6c-1081">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1081">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegpointtransforms"></a><span data-ttu-id="70d6c-1082">PropertyTagJPEGPointTransforms</span><span class="sxs-lookup"><span data-stu-id="70d6c-1082">PropertyTagJPEGPointTransforms</span></span>

<span data-ttu-id="70d6c-1083">針對每個色彩元件，該元件的點變換值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1083">For each color component, a point transformation value for that component.</span></span> <span data-ttu-id="70d6c-1084">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1084">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-1085">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1085">Property info</span></span> | <span data-ttu-id="70d6c-1086">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1086">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-1087">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1087">Tag</span></span>   | <span data-ttu-id="70d6c-1088">0x0206</span><span class="sxs-lookup"><span data-stu-id="70d6c-1088">0x0206</span></span>                                   |
| <span data-ttu-id="70d6c-1089">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1089">Type</span></span>  | <span data-ttu-id="70d6c-1090">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1090">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="70d6c-1091">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1091">Count</span></span> | <span data-ttu-id="70d6c-1092">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1092">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegqtables"></a><span data-ttu-id="70d6c-1093">PropertyTagJPEGQTables</span><span class="sxs-lookup"><span data-stu-id="70d6c-1093">PropertyTagJPEGQTables</span></span>

<span data-ttu-id="70d6c-1094">針對每個色彩元件，該元件的量化資料表位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1094">For each color component, the offset to the quantization table for that component.</span></span> <span data-ttu-id="70d6c-1095">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1095">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-1096">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1096">Property info</span></span> | <span data-ttu-id="70d6c-1097">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1097">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-1098">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1098">Tag</span></span>   | <span data-ttu-id="70d6c-1099">0x0207</span><span class="sxs-lookup"><span data-stu-id="70d6c-1099">0x0207</span></span>                                   |
| <span data-ttu-id="70d6c-1100">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1100">Type</span></span>  | <span data-ttu-id="70d6c-1101">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1101">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="70d6c-1102">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1102">Count</span></span> | <span data-ttu-id="70d6c-1103">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1103">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegdctables"></a><span data-ttu-id="70d6c-1104">PropertyTagJPEGDCTables</span><span class="sxs-lookup"><span data-stu-id="70d6c-1104">PropertyTagJPEGDCTables</span></span>

<span data-ttu-id="70d6c-1105">針對每個色彩元件，DC Huffman 資料表的位移 (或不失真的 Huffman 資料表) 該元件。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1105">For each color component, the offset to the DC Huffman table (or lossless Huffman table) for that component.</span></span> <span data-ttu-id="70d6c-1106">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1106">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-1107">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1107">Property info</span></span> | <span data-ttu-id="70d6c-1108">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1108">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-1109">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1109">Tag</span></span>   | <span data-ttu-id="70d6c-1110">0x0208</span><span class="sxs-lookup"><span data-stu-id="70d6c-1110">0x0208</span></span>                                   |
| <span data-ttu-id="70d6c-1111">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1111">Type</span></span>  | <span data-ttu-id="70d6c-1112">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1112">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="70d6c-1113">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1113">Count</span></span> | <span data-ttu-id="70d6c-1114">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1114">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegactables"></a><span data-ttu-id="70d6c-1115">PropertyTagJPEGACTables</span><span class="sxs-lookup"><span data-stu-id="70d6c-1115">PropertyTagJPEGACTables</span></span>

<span data-ttu-id="70d6c-1116">針對每個色彩元件，這是該元件之 AC Huffman 資料表的位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1116">For each color component, the offset to the AC Huffman table for that component.</span></span> <span data-ttu-id="70d6c-1117">另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1117">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-1118">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1118">Property info</span></span> | <span data-ttu-id="70d6c-1119">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1119">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="70d6c-1120">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1120">Tag</span></span>   | <span data-ttu-id="70d6c-1121">0x0209</span><span class="sxs-lookup"><span data-stu-id="70d6c-1121">0x0209</span></span>                                   |
| <span data-ttu-id="70d6c-1122">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1122">Type</span></span>  | <span data-ttu-id="70d6c-1123">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1123">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="70d6c-1124">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1124">Count</span></span> | <span data-ttu-id="70d6c-1125">每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1125">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagycbcrcoefficients"></a><span data-ttu-id="70d6c-1126">PropertyTagYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="70d6c-1126">PropertyTagYCbCrCoefficients</span></span>

<span data-ttu-id="70d6c-1127">從 RGB 轉換成 YCbCr 影像資料的係數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1127">Coefficients for transformation from RGB to YCbCr image data.</span></span>



| <span data-ttu-id="70d6c-1128">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1128">Property info</span></span> | <span data-ttu-id="70d6c-1129">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1129">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1130">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1130">Tag</span></span>   | <span data-ttu-id="70d6c-1131">0x0211</span><span class="sxs-lookup"><span data-stu-id="70d6c-1131">0x0211</span></span>                  |
| <span data-ttu-id="70d6c-1132">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1132">Type</span></span>  | <span data-ttu-id="70d6c-1133">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1133">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1134">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1134">Count</span></span> | <span data-ttu-id="70d6c-1135">3</span><span class="sxs-lookup"><span data-stu-id="70d6c-1135">3</span></span>                       |



 

## <a name="propertytagycbcrsubsampling"></a><span data-ttu-id="70d6c-1136">PropertyTagYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="70d6c-1136">PropertyTagYCbCrSubsampling</span></span>

<span data-ttu-id="70d6c-1137">相對於亮度元件的色度元件取樣率。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1137">Sampling ratio of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="70d6c-1138">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1138">Property info</span></span> | <span data-ttu-id="70d6c-1139">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1139">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1140">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1140">Tag</span></span>   | <span data-ttu-id="70d6c-1141">0x0212</span><span class="sxs-lookup"><span data-stu-id="70d6c-1141">0x0212</span></span>               |
| <span data-ttu-id="70d6c-1142">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1142">Type</span></span>  | <span data-ttu-id="70d6c-1143">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1143">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1144">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1144">Count</span></span> | <span data-ttu-id="70d6c-1145">2</span><span class="sxs-lookup"><span data-stu-id="70d6c-1145">2</span></span>                    |



 

## <a name="propertytagycbcrpositioning"></a><span data-ttu-id="70d6c-1146">PropertyTagYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="70d6c-1146">PropertyTagYCbCrPositioning</span></span>

<span data-ttu-id="70d6c-1147">色度元件相對於亮度元件的位置。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1147">Position of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="70d6c-1148">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1148">Property info</span></span> | <span data-ttu-id="70d6c-1149">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1149">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1150">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1150">Tag</span></span>   | <span data-ttu-id="70d6c-1151">0x0213</span><span class="sxs-lookup"><span data-stu-id="70d6c-1151">0x0213</span></span>               |
| <span data-ttu-id="70d6c-1152">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1152">Type</span></span>  | <span data-ttu-id="70d6c-1153">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1153">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1154">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1154">Count</span></span> | <span data-ttu-id="70d6c-1155">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1155">1</span></span>                    |



 

## <a name="propertytagrefblackwhite"></a><span data-ttu-id="70d6c-1156">PropertyTagREFBlackWhite</span><span class="sxs-lookup"><span data-stu-id="70d6c-1156">PropertyTagREFBlackWhite</span></span>

<span data-ttu-id="70d6c-1157">參考黑色點值和參考點值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1157">Reference black point value and reference white point value.</span></span>



| <span data-ttu-id="70d6c-1158">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1158">Property info</span></span> | <span data-ttu-id="70d6c-1159">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1159">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1160">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1160">Tag</span></span>   | <span data-ttu-id="70d6c-1161">0x0214</span><span class="sxs-lookup"><span data-stu-id="70d6c-1161">0x0214</span></span>                  |
| <span data-ttu-id="70d6c-1162">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1162">Type</span></span>  | <span data-ttu-id="70d6c-1163">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1163">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1164">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1164">Count</span></span> | <span data-ttu-id="70d6c-1165">6</span><span class="sxs-lookup"><span data-stu-id="70d6c-1165">6</span></span>                       |



 

## <a name="propertytaggamma"></a><span data-ttu-id="70d6c-1166">PropertyTagGamma</span><span class="sxs-lookup"><span data-stu-id="70d6c-1166">PropertyTagGamma</span></span>

<span data-ttu-id="70d6c-1167">附加至影像的 Gamma 值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1167">Gamma value attached to the image.</span></span> <span data-ttu-id="70d6c-1168">Gamma 值會儲存為有理數 (成對的 **long**) ，且分子為100000。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1168">The gamma value is stored as a rational number (pair of **long**) with a numerator of 100000.</span></span> <span data-ttu-id="70d6c-1169">例如，將 gamma 值2.2 儲存為配對 (100000，45455) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1169">For example, a gamma value of 2.2 is stored as the pair (100000, 45455).</span></span>



| <span data-ttu-id="70d6c-1170">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1170">Property info</span></span> | <span data-ttu-id="70d6c-1171">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1171">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1172">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1172">Tag</span></span>   | <span data-ttu-id="70d6c-1173">0x0301</span><span class="sxs-lookup"><span data-stu-id="70d6c-1173">0x0301</span></span>                  |
| <span data-ttu-id="70d6c-1174">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1174">Type</span></span>  | <span data-ttu-id="70d6c-1175">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1175">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1176">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1176">Count</span></span> | <span data-ttu-id="70d6c-1177">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1177">1</span></span>                       |



 

## <a name="propertytagiccprofiledescriptor"></a><span data-ttu-id="70d6c-1178">PropertyTagICCProfileDescriptor</span><span class="sxs-lookup"><span data-stu-id="70d6c-1178">PropertyTagICCProfileDescriptor</span></span>

<span data-ttu-id="70d6c-1179">識別 ICC 設定檔的以 Null 結束的字元字串。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1179">Null-terminated character string that identifies an ICC profile.</span></span>



| <span data-ttu-id="70d6c-1180">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1180">Property info</span></span> | <span data-ttu-id="70d6c-1181">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1181">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1182">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1182">Tag</span></span>   | <span data-ttu-id="70d6c-1183">0x0302</span><span class="sxs-lookup"><span data-stu-id="70d6c-1183">0x0302</span></span>                                             |
| <span data-ttu-id="70d6c-1184">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1184">Type</span></span>  | <span data-ttu-id="70d6c-1185">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1185">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1186">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1186">Count</span></span> | <span data-ttu-id="70d6c-1187">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1187">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagsrgbrenderingintent"></a><span data-ttu-id="70d6c-1188">PropertyTagSRGBRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="70d6c-1188">PropertyTagSRGBRenderingIntent</span></span>

<span data-ttu-id="70d6c-1189">應如何依照國際色彩協會 (ICC) 的定義來顯示影像。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1189">How the image should be displayed as defined by the International Color Consortium (ICC).</span></span> <span data-ttu-id="70d6c-1190">如果使用設定為 **TRUE** 的 *useEmbeddedColorManagement* 參數來建立 gdi +[**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件，則 gdi + 會根據指定的轉譯意圖呈現影像。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1190">If a GDI+  [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object is constructed with the *useEmbeddedColorManagement* parameter set to **TRUE**, then GDI+ renders the image according to the specified rendering intent.</span></span> <span data-ttu-id="70d6c-1191">意圖可以設定為可感知、相對色度、飽和度或絕對色度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1191">The intent can be set to perceptual, relative colorimetric, saturation, or absolute colorimetric.</span></span>

-   <span data-ttu-id="70d6c-1192">適用于相片的可感知意圖可針對顯示裝置範圍提供良好的調整，但代價是會降低色度的精確度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1192">Perceptual intent, which is suitable for photographs, gives good adaptation to the display device gamut at the expense of colorimetric accuracy.</span></span>
-   <span data-ttu-id="70d6c-1193">相對色度意圖適用于影像 (例如，標誌) ，其需要相對於顯示裝置的白色點進行色彩外觀比對。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1193">Relative colorimetric intent is suitable for images (for example, logos) that require color appearance matching that is relative to the display device white point.</span></span>
-   <span data-ttu-id="70d6c-1194">飽和度意圖適用于圖表和圖形，可保留色調和亮度的飽和度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1194">Saturation intent, which is suitable for charts and graphs, preserves saturation at the expense of hue and lightness.</span></span>
-   <span data-ttu-id="70d6c-1195">絕對色度意圖適用于證明 (預覽版的影像會以不同的顯示裝置) ，需要保留絕對 colorimetry。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1195">Absolute colorimetric intent is suitable for proofs (previews of images destined for a different display device) that require preservation of absolute colorimetry.</span></span>



<span data-ttu-id="70d6c-1196">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1196">Tag</span></span>

<span data-ttu-id="70d6c-1197">0x0303</span><span class="sxs-lookup"><span data-stu-id="70d6c-1197">0x0303</span></span>

<span data-ttu-id="70d6c-1198">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1198">Type</span></span>

<span data-ttu-id="70d6c-1199">BYTE</span><span class="sxs-lookup"><span data-stu-id="70d6c-1199">BYTE</span></span>

<span data-ttu-id="70d6c-1200">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1200">Count</span></span>

<span data-ttu-id="70d6c-1201">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1201">1</span></span>

<span data-ttu-id="70d6c-1202">0-感知 1-相對色度 2-飽和度 3-絕對色度</span><span class="sxs-lookup"><span data-stu-id="70d6c-1202">0 - perceptual 1 - relative colorimetric 2 - saturation 3 - absolute colorimetric</span></span>



 

## <a name="propertytagimagetitle"></a><span data-ttu-id="70d6c-1203">PropertyTagImageTitle</span><span class="sxs-lookup"><span data-stu-id="70d6c-1203">PropertyTagImageTitle</span></span>

<span data-ttu-id="70d6c-1204">以 Null 結束的字元字串，指定影像的標題。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1204">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="70d6c-1205">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1205">Property info</span></span> | <span data-ttu-id="70d6c-1206">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1206">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1207">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1207">Tag</span></span>   | <span data-ttu-id="70d6c-1208">0x0320</span><span class="sxs-lookup"><span data-stu-id="70d6c-1208">0x0320</span></span>                                             |
| <span data-ttu-id="70d6c-1209">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1209">Type</span></span>  | <span data-ttu-id="70d6c-1210">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1210">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1211">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1211">Count</span></span> | <span data-ttu-id="70d6c-1212">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1212">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagresolutionxunit"></a><span data-ttu-id="70d6c-1213">PropertyTagResolutionXUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-1213">PropertyTagResolutionXUnit</span></span>

<span data-ttu-id="70d6c-1214">要顯示水準解析度的單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1214">Units in which to display horizontal resolution.</span></span>



<span data-ttu-id="70d6c-1215">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1215">Tag</span></span>

<span data-ttu-id="70d6c-1216">0x5001</span><span class="sxs-lookup"><span data-stu-id="70d6c-1216">0x5001</span></span>

<span data-ttu-id="70d6c-1217">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1217">Type</span></span>

<span data-ttu-id="70d6c-1218">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1218">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-1219">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1219">Count</span></span>

<span data-ttu-id="70d6c-1220">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1220">1</span></span>

<span data-ttu-id="70d6c-1221">1-圖元/每英寸 2-圖元/每釐米</span><span class="sxs-lookup"><span data-stu-id="70d6c-1221">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionyunit"></a><span data-ttu-id="70d6c-1222">PropertyTagResolutionYUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-1222">PropertyTagResolutionYUnit</span></span>

<span data-ttu-id="70d6c-1223">顯示垂直解析度的單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1223">Units in which to display vertical resolution.</span></span>



<span data-ttu-id="70d6c-1224">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1224">Tag</span></span>

<span data-ttu-id="70d6c-1225">0x5002</span><span class="sxs-lookup"><span data-stu-id="70d6c-1225">0x5002</span></span>

<span data-ttu-id="70d6c-1226">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1226">Type</span></span>

<span data-ttu-id="70d6c-1227">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1227">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-1228">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1228">Count</span></span>

<span data-ttu-id="70d6c-1229">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1229">1</span></span>

<span data-ttu-id="70d6c-1230">1-圖元/每英寸 2-圖元/每釐米</span><span class="sxs-lookup"><span data-stu-id="70d6c-1230">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionxlengthunit"></a><span data-ttu-id="70d6c-1231">PropertyTagResolutionXLengthUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-1231">PropertyTagResolutionXLengthUnit</span></span>

<span data-ttu-id="70d6c-1232">要顯示影像寬度的單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1232">Units in which to display the image width.</span></span>



<span data-ttu-id="70d6c-1233">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1233">Tag</span></span>

<span data-ttu-id="70d6c-1234">0x5003</span><span class="sxs-lookup"><span data-stu-id="70d6c-1234">0x5003</span></span>

<span data-ttu-id="70d6c-1235">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1235">Type</span></span>

<span data-ttu-id="70d6c-1236">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1236">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-1237">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1237">Count</span></span>

<span data-ttu-id="70d6c-1238">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1238">1</span></span>

<span data-ttu-id="70d6c-1239">1-英寸 2-x 3-點 4-十二點活字 5-欄</span><span class="sxs-lookup"><span data-stu-id="70d6c-1239">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagresolutionylengthunit"></a><span data-ttu-id="70d6c-1240">PropertyTagResolutionYLengthUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-1240">PropertyTagResolutionYLengthUnit</span></span>

<span data-ttu-id="70d6c-1241">要顯示影像高度的單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1241">Units in which to display the image height.</span></span>



<span data-ttu-id="70d6c-1242">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1242">Tag</span></span>

<span data-ttu-id="70d6c-1243">0x5004</span><span class="sxs-lookup"><span data-stu-id="70d6c-1243">0x5004</span></span>

<span data-ttu-id="70d6c-1244">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1244">Type</span></span>

<span data-ttu-id="70d6c-1245">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1245">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-1246">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1246">Count</span></span>

<span data-ttu-id="70d6c-1247">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1247">1</span></span>

<span data-ttu-id="70d6c-1248">1-英寸 2-x 3-點 4-十二點活字 5-欄</span><span class="sxs-lookup"><span data-stu-id="70d6c-1248">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagprintflags"></a><span data-ttu-id="70d6c-1249">PropertyTagPrintFlags</span><span class="sxs-lookup"><span data-stu-id="70d6c-1249">PropertyTagPrintFlags</span></span>

<span data-ttu-id="70d6c-1250">指定列印選項的單位元組布林值順序。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1250">Sequence of one-byte Boolean values that specify printing options.</span></span>



| <span data-ttu-id="70d6c-1251">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1251">Property info</span></span> | <span data-ttu-id="70d6c-1252">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1252">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1253">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1253">Tag</span></span>   | <span data-ttu-id="70d6c-1254">0x5005</span><span class="sxs-lookup"><span data-stu-id="70d6c-1254">0x5005</span></span>               |
| <span data-ttu-id="70d6c-1255">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1255">Type</span></span>  | <span data-ttu-id="70d6c-1256">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1256">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="70d6c-1257">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1257">Count</span></span> | <span data-ttu-id="70d6c-1258">旗標數目</span><span class="sxs-lookup"><span data-stu-id="70d6c-1258">Number of flags</span></span>      |



 

## <a name="propertytagprintflagsversion"></a><span data-ttu-id="70d6c-1259">PropertyTagPrintFlagsVersion</span><span class="sxs-lookup"><span data-stu-id="70d6c-1259">PropertyTagPrintFlagsVersion</span></span>

<span data-ttu-id="70d6c-1260">列印旗標版本。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1260">Print flags version.</span></span>



| <span data-ttu-id="70d6c-1261">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1261">Property info</span></span> | <span data-ttu-id="70d6c-1262">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1262">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1263">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1263">Tag</span></span>   | <span data-ttu-id="70d6c-1264">0x5006</span><span class="sxs-lookup"><span data-stu-id="70d6c-1264">0x5006</span></span>               |
| <span data-ttu-id="70d6c-1265">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1265">Type</span></span>  | <span data-ttu-id="70d6c-1266">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1266">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1267">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1267">Count</span></span> | <span data-ttu-id="70d6c-1268">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1268">1</span></span>                    |



 

## <a name="propertytagprintflagscrop"></a><span data-ttu-id="70d6c-1269">PropertyTagPrintFlagsCrop</span><span class="sxs-lookup"><span data-stu-id="70d6c-1269">PropertyTagPrintFlagsCrop</span></span>

<span data-ttu-id="70d6c-1270">列印旗標中心裁剪標記。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1270">Print flags center crop marks.</span></span>



| <span data-ttu-id="70d6c-1271">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1271">Property info</span></span> | <span data-ttu-id="70d6c-1272">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1272">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1273">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1273">Tag</span></span>   | <span data-ttu-id="70d6c-1274">0x5007</span><span class="sxs-lookup"><span data-stu-id="70d6c-1274">0x5007</span></span>              |
| <span data-ttu-id="70d6c-1275">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1275">Type</span></span>  | <span data-ttu-id="70d6c-1276">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1276">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="70d6c-1277">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1277">Count</span></span> | <span data-ttu-id="70d6c-1278">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1278">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidth"></a><span data-ttu-id="70d6c-1279">PropertyTagPrintFlagsBleedWidth</span><span class="sxs-lookup"><span data-stu-id="70d6c-1279">PropertyTagPrintFlagsBleedWidth</span></span>

<span data-ttu-id="70d6c-1280">列印旗標出血寬度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1280">Print flags bleed width.</span></span>



| <span data-ttu-id="70d6c-1281">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1281">Property info</span></span> | <span data-ttu-id="70d6c-1282">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1282">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1283">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1283">Tag</span></span>   | <span data-ttu-id="70d6c-1284">0x5008</span><span class="sxs-lookup"><span data-stu-id="70d6c-1284">0x5008</span></span>              |
| <span data-ttu-id="70d6c-1285">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1285">Type</span></span>  | <span data-ttu-id="70d6c-1286">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1286">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1287">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1287">Count</span></span> | <span data-ttu-id="70d6c-1288">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1288">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a><span data-ttu-id="70d6c-1289">PropertyTagPrintFlagsBleedWidthScale</span><span class="sxs-lookup"><span data-stu-id="70d6c-1289">PropertyTagPrintFlagsBleedWidthScale</span></span>

<span data-ttu-id="70d6c-1290">列印旗標出血寬度尺規。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1290">Print flags bleed width scale.</span></span>



| <span data-ttu-id="70d6c-1291">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1291">Property info</span></span> | <span data-ttu-id="70d6c-1292">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1292">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1293">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1293">Tag</span></span>   | <span data-ttu-id="70d6c-1294">0x5009</span><span class="sxs-lookup"><span data-stu-id="70d6c-1294">0x5009</span></span>               |
| <span data-ttu-id="70d6c-1295">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1295">Type</span></span>  | <span data-ttu-id="70d6c-1296">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1296">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1297">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1297">Count</span></span> | <span data-ttu-id="70d6c-1298">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1298">1</span></span>                    |



 

## <a name="propertytaghalftonelpi"></a><span data-ttu-id="70d6c-1299">PropertyTagHalftoneLPI</span><span class="sxs-lookup"><span data-stu-id="70d6c-1299">PropertyTagHalftoneLPI</span></span>

<span data-ttu-id="70d6c-1300">筆墨的螢幕頻率（以每英寸的行數為單位）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1300">Ink's screen frequency, in lines per inch.</span></span>



| <span data-ttu-id="70d6c-1301">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1301">Property info</span></span> | <span data-ttu-id="70d6c-1302">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1302">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1303">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1303">Tag</span></span>   | <span data-ttu-id="70d6c-1304">0x500A</span><span class="sxs-lookup"><span data-stu-id="70d6c-1304">0x500A</span></span>                  |
| <span data-ttu-id="70d6c-1305">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1305">Type</span></span>  | <span data-ttu-id="70d6c-1306">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1306">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1307">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1307">Count</span></span> | <span data-ttu-id="70d6c-1308">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1308">1</span></span>                       |



 

## <a name="propertytaghalftonelpiunit"></a><span data-ttu-id="70d6c-1309">PropertyTagHalftoneLPIUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-1309">PropertyTagHalftoneLPIUnit</span></span>

<span data-ttu-id="70d6c-1310">螢幕頻率的單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1310">Units for the screen frequency.</span></span>



<span data-ttu-id="70d6c-1311">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1311">Tag</span></span>

<span data-ttu-id="70d6c-1312">0x500B</span><span class="sxs-lookup"><span data-stu-id="70d6c-1312">0x500B</span></span>

<span data-ttu-id="70d6c-1313">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1313">Type</span></span>

<span data-ttu-id="70d6c-1314">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1314">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-1315">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1315">Count</span></span>

<span data-ttu-id="70d6c-1316">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1316">1</span></span>

<span data-ttu-id="70d6c-1317">1-每英寸2行2行（每個釐米）</span><span class="sxs-lookup"><span data-stu-id="70d6c-1317">1 - lines per inch 2 - lines per centimeter</span></span>



 

## <a name="propertytaghalftonedegree"></a><span data-ttu-id="70d6c-1318">PropertyTagHalftoneDegree</span><span class="sxs-lookup"><span data-stu-id="70d6c-1318">PropertyTagHalftoneDegree</span></span>

<span data-ttu-id="70d6c-1319">螢幕的角度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1319">Angle for screen.</span></span>



| <span data-ttu-id="70d6c-1320">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1320">Property info</span></span> | <span data-ttu-id="70d6c-1321">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1321">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1322">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1322">Tag</span></span>   | <span data-ttu-id="70d6c-1323">0x500C</span><span class="sxs-lookup"><span data-stu-id="70d6c-1323">0x500C</span></span>                  |
| <span data-ttu-id="70d6c-1324">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1324">Type</span></span>  | <span data-ttu-id="70d6c-1325">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1325">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1326">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1326">Count</span></span> | <span data-ttu-id="70d6c-1327">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1327">1</span></span>                       |



 

## <a name="propertytaghalftoneshape"></a><span data-ttu-id="70d6c-1328">PropertyTagHalftoneShape</span><span class="sxs-lookup"><span data-stu-id="70d6c-1328">PropertyTagHalftoneShape</span></span>

<span data-ttu-id="70d6c-1329">半色調點的形狀。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1329">Shape of the halftone dots.</span></span>



<span data-ttu-id="70d6c-1330">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1330">Tag</span></span>

<span data-ttu-id="70d6c-1331">0x500D</span><span class="sxs-lookup"><span data-stu-id="70d6c-1331">0x500D</span></span>

<span data-ttu-id="70d6c-1332">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1332">Type</span></span>

<span data-ttu-id="70d6c-1333">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1333">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-1334">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1334">Count</span></span>

<span data-ttu-id="70d6c-1335">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1335">1</span></span>

<span data-ttu-id="70d6c-1336">0-四捨五入 1-橢圓形 2-行 3-方形 4-交叉 6-菱形</span><span class="sxs-lookup"><span data-stu-id="70d6c-1336">0 - round 1 - ellipse 2 - line 3 - square 4 - cross 6 - diamond</span></span>



 

## <a name="propertytaghalftonemisc"></a><span data-ttu-id="70d6c-1337">PropertyTagHalftoneMisc</span><span class="sxs-lookup"><span data-stu-id="70d6c-1337">PropertyTagHalftoneMisc</span></span>

<span data-ttu-id="70d6c-1338">其他半色調資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1338">Miscellaneous halftone information.</span></span>



| <span data-ttu-id="70d6c-1339">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1339">Property info</span></span> | <span data-ttu-id="70d6c-1340">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1340">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1341">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1341">Tag</span></span>   | <span data-ttu-id="70d6c-1342">0x500E</span><span class="sxs-lookup"><span data-stu-id="70d6c-1342">0x500E</span></span>              |
| <span data-ttu-id="70d6c-1343">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1343">Type</span></span>  | <span data-ttu-id="70d6c-1344">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1344">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1345">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1345">Count</span></span> | <span data-ttu-id="70d6c-1346">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1346">1</span></span>                   |



 

## <a name="propertytaghalftonescreen"></a><span data-ttu-id="70d6c-1347">PropertyTagHalftoneScreen</span><span class="sxs-lookup"><span data-stu-id="70d6c-1347">PropertyTagHalftoneScreen</span></span>

<span data-ttu-id="70d6c-1348">指定是否要使用印表機預設畫面的布林值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1348">Boolean value that specifies whether to use the printer's default screens.</span></span>



<span data-ttu-id="70d6c-1349">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1349">Tag</span></span>

<span data-ttu-id="70d6c-1350">0x500F</span><span class="sxs-lookup"><span data-stu-id="70d6c-1350">0x500F</span></span>

<span data-ttu-id="70d6c-1351">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1351">Type</span></span>

<span data-ttu-id="70d6c-1352">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1352">PropertyTagTypeByte</span></span>

<span data-ttu-id="70d6c-1353">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1353">Count</span></span>

<span data-ttu-id="70d6c-1354">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1354">1</span></span>

<span data-ttu-id="70d6c-1355">1-使用印表機的預設畫面 2-其他</span><span class="sxs-lookup"><span data-stu-id="70d6c-1355">1 - use printer's default screens 2 - other</span></span>



 

## <a name="propertytagjpegquality"></a><span data-ttu-id="70d6c-1356">PropertyTagJPEGQuality</span><span class="sxs-lookup"><span data-stu-id="70d6c-1356">PropertyTagJPEGQuality</span></span>

<span data-ttu-id="70d6c-1357">Adobe Photoshop 格式所使用的私用標記。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1357">Private tag used by the Adobe Photoshop format.</span></span> <span data-ttu-id="70d6c-1358">不提供公開使用。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1358">Not for public use.</span></span>



| <span data-ttu-id="70d6c-1359">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1359">Property info</span></span> | <span data-ttu-id="70d6c-1360">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1360">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1361">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1361">Tag</span></span>   | <span data-ttu-id="70d6c-1362">0x5010</span><span class="sxs-lookup"><span data-stu-id="70d6c-1362">0x5010</span></span>               |
| <span data-ttu-id="70d6c-1363">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1363">Type</span></span>  | <span data-ttu-id="70d6c-1364">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1364">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1365">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1365">Count</span></span> | <span data-ttu-id="70d6c-1366">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-1366">Any</span></span>                  |



 

## <a name="propertytaggridsize"></a><span data-ttu-id="70d6c-1367">PropertyTagGridSize</span><span class="sxs-lookup"><span data-stu-id="70d6c-1367">PropertyTagGridSize</span></span>

<span data-ttu-id="70d6c-1368">格線和輔助線的相關資訊區塊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1368">Block of information about grids and guides.</span></span>



| <span data-ttu-id="70d6c-1369">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1369">Property info</span></span> | <span data-ttu-id="70d6c-1370">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1370">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-1371">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1371">Tag</span></span>   | <span data-ttu-id="70d6c-1372">0x5011</span><span class="sxs-lookup"><span data-stu-id="70d6c-1372">0x5011</span></span>                   |
| <span data-ttu-id="70d6c-1373">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1373">Type</span></span>  | <span data-ttu-id="70d6c-1374">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-1374">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-1375">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1375">Count</span></span> | <span data-ttu-id="70d6c-1376">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-1376">Any</span></span>                      |



 

## <a name="propertytagthumbnailformat"></a><span data-ttu-id="70d6c-1377">PropertyTagThumbnailFormat</span><span class="sxs-lookup"><span data-stu-id="70d6c-1377">PropertyTagThumbnailFormat</span></span>

<span data-ttu-id="70d6c-1378">縮圖影像的格式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1378">Format of the thumbnail image.</span></span>



<span data-ttu-id="70d6c-1379">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1379">Tag</span></span>

<span data-ttu-id="70d6c-1380">0x5012</span><span class="sxs-lookup"><span data-stu-id="70d6c-1380">0x5012</span></span>

<span data-ttu-id="70d6c-1381">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1381">Type</span></span>

<span data-ttu-id="70d6c-1382">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1382">PropertyTagTypeLong</span></span>

<span data-ttu-id="70d6c-1383">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1383">Count</span></span>

<span data-ttu-id="70d6c-1384">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1384">1</span></span>

<span data-ttu-id="70d6c-1385">0-原始 RGB 1-JPEG</span><span class="sxs-lookup"><span data-stu-id="70d6c-1385">0 - raw RGB 1 - JPEG</span></span>



 

## <a name="propertytagthumbnailwidth"></a><span data-ttu-id="70d6c-1386">PropertyTagThumbnailWidth</span><span class="sxs-lookup"><span data-stu-id="70d6c-1386">PropertyTagThumbnailWidth</span></span>

<span data-ttu-id="70d6c-1387">縮圖影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1387">Width, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1388">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1388">Property info</span></span> | <span data-ttu-id="70d6c-1389">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1389">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1390">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1390">Tag</span></span>   | <span data-ttu-id="70d6c-1391">0x5013</span><span class="sxs-lookup"><span data-stu-id="70d6c-1391">0x5013</span></span>              |
| <span data-ttu-id="70d6c-1392">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1392">Type</span></span>  | <span data-ttu-id="70d6c-1393">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1393">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1394">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1394">Count</span></span> | <span data-ttu-id="70d6c-1395">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1395">1</span></span>                   |



 

## <a name="propertytagthumbnailheight"></a><span data-ttu-id="70d6c-1396">PropertyTagThumbnailHeight</span><span class="sxs-lookup"><span data-stu-id="70d6c-1396">PropertyTagThumbnailHeight</span></span>

<span data-ttu-id="70d6c-1397">縮圖影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1397">Height, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1398">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1398">Property info</span></span> | <span data-ttu-id="70d6c-1399">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1399">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1400">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1400">Tag</span></span>   | <span data-ttu-id="70d6c-1401">0x5014</span><span class="sxs-lookup"><span data-stu-id="70d6c-1401">0x5014</span></span>              |
| <span data-ttu-id="70d6c-1402">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1402">Type</span></span>  | <span data-ttu-id="70d6c-1403">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1403">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1404">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1404">Count</span></span> | <span data-ttu-id="70d6c-1405">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1405">1</span></span>                   |



 

## <a name="propertytagthumbnailcolordepth"></a><span data-ttu-id="70d6c-1406">PropertyTagThumbnailColorDepth</span><span class="sxs-lookup"><span data-stu-id="70d6c-1406">PropertyTagThumbnailColorDepth</span></span>

<span data-ttu-id="70d6c-1407">縮圖影像的每一像素位元數 (BPP) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1407">bits per pixel (BPP) for the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1408">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1408">Property info</span></span> | <span data-ttu-id="70d6c-1409">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1409">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1410">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1410">Tag</span></span>   | <span data-ttu-id="70d6c-1411">0x5015</span><span class="sxs-lookup"><span data-stu-id="70d6c-1411">0x5015</span></span>               |
| <span data-ttu-id="70d6c-1412">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1412">Type</span></span>  | <span data-ttu-id="70d6c-1413">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1413">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1414">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1414">Count</span></span> | <span data-ttu-id="70d6c-1415">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1415">1</span></span>                    |



 

## <a name="propertytagthumbnailplanes"></a><span data-ttu-id="70d6c-1416">PropertyTagThumbnailPlanes</span><span class="sxs-lookup"><span data-stu-id="70d6c-1416">PropertyTagThumbnailPlanes</span></span>

<span data-ttu-id="70d6c-1417">縮圖影像的色彩平面數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1417">Number of color planes for the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1418">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1418">Property info</span></span> | <span data-ttu-id="70d6c-1419">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1419">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1420">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1420">Tag</span></span>   | <span data-ttu-id="70d6c-1421">0x5016</span><span class="sxs-lookup"><span data-stu-id="70d6c-1421">0x5016</span></span>               |
| <span data-ttu-id="70d6c-1422">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1422">Type</span></span>  | <span data-ttu-id="70d6c-1423">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1423">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1424">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1424">Count</span></span> | <span data-ttu-id="70d6c-1425">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1425">1</span></span>                    |



 

## <a name="propertytagthumbnailrawbytes"></a><span data-ttu-id="70d6c-1426">PropertyTagThumbnailRawBytes</span><span class="sxs-lookup"><span data-stu-id="70d6c-1426">PropertyTagThumbnailRawBytes</span></span>

<span data-ttu-id="70d6c-1427">圖元資料列之間的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1427">Byte offset between rows of pixel data.</span></span>



| <span data-ttu-id="70d6c-1428">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1428">Property info</span></span> | <span data-ttu-id="70d6c-1429">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1429">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1430">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1430">Tag</span></span>   | <span data-ttu-id="70d6c-1431">0x5017</span><span class="sxs-lookup"><span data-stu-id="70d6c-1431">0x5017</span></span>              |
| <span data-ttu-id="70d6c-1432">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1432">Type</span></span>  | <span data-ttu-id="70d6c-1433">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1433">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1434">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1434">Count</span></span> | <span data-ttu-id="70d6c-1435">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1435">1</span></span>                   |



 

## <a name="propertytagthumbnailsize"></a><span data-ttu-id="70d6c-1436">PropertyTagThumbnailSize</span><span class="sxs-lookup"><span data-stu-id="70d6c-1436">PropertyTagThumbnailSize</span></span>

<span data-ttu-id="70d6c-1437">縮圖影像的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1437">Total size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1438">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1438">Property info</span></span> | <span data-ttu-id="70d6c-1439">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1439">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1440">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1440">Tag</span></span>   | <span data-ttu-id="70d6c-1441">0x5018</span><span class="sxs-lookup"><span data-stu-id="70d6c-1441">0x5018</span></span>              |
| <span data-ttu-id="70d6c-1442">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1442">Type</span></span>  | <span data-ttu-id="70d6c-1443">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1443">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1444">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1444">Count</span></span> | <span data-ttu-id="70d6c-1445">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1445">1</span></span>                   |



 

## <a name="propertytagthumbnailcompressedsize"></a><span data-ttu-id="70d6c-1446">PropertyTagThumbnailCompressedSize</span><span class="sxs-lookup"><span data-stu-id="70d6c-1446">PropertyTagThumbnailCompressedSize</span></span>

<span data-ttu-id="70d6c-1447">縮圖影像的壓縮大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1447">Compressed size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1448">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1448">Property info</span></span> | <span data-ttu-id="70d6c-1449">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1449">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1450">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1450">Tag</span></span>   | <span data-ttu-id="70d6c-1451">0x5019</span><span class="sxs-lookup"><span data-stu-id="70d6c-1451">0x5019</span></span>              |
| <span data-ttu-id="70d6c-1452">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1452">Type</span></span>  | <span data-ttu-id="70d6c-1453">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1453">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1454">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1454">Count</span></span> | <span data-ttu-id="70d6c-1455">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1455">1</span></span>                   |



 

## <a name="propertytagcolortransferfunction"></a><span data-ttu-id="70d6c-1456">PropertyTagColorTransferFunction</span><span class="sxs-lookup"><span data-stu-id="70d6c-1456">PropertyTagColorTransferFunction</span></span>

<span data-ttu-id="70d6c-1457">指定色彩傳送函式之值的資料表。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1457">Table of values that specify color transfer functions.</span></span>



| <span data-ttu-id="70d6c-1458">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1458">Property info</span></span> | <span data-ttu-id="70d6c-1459">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1459">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-1460">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1460">Tag</span></span>   | <span data-ttu-id="70d6c-1461">0x501A</span><span class="sxs-lookup"><span data-stu-id="70d6c-1461">0x501A</span></span>                   |
| <span data-ttu-id="70d6c-1462">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1462">Type</span></span>  | <span data-ttu-id="70d6c-1463">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-1463">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-1464">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1464">Count</span></span> | <span data-ttu-id="70d6c-1465">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-1465">Any</span></span>                      |



 

## <a name="propertytagthumbnaildata"></a><span data-ttu-id="70d6c-1466">PropertyTagThumbnailData</span><span class="sxs-lookup"><span data-stu-id="70d6c-1466">PropertyTagThumbnailData</span></span>

<span data-ttu-id="70d6c-1467">JPEG 或 RGB 格式的原始縮圖位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1467">Raw thumbnail bits in JPEG or RGB format.</span></span> <span data-ttu-id="70d6c-1468">取決於 PropertyTagThumbnailFormat。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1468">Depends on PropertyTagThumbnailFormat.</span></span>



| <span data-ttu-id="70d6c-1469">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1469">Property info</span></span> | <span data-ttu-id="70d6c-1470">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1470">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1471">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1471">Tag</span></span>   | <span data-ttu-id="70d6c-1472">0x501B</span><span class="sxs-lookup"><span data-stu-id="70d6c-1472">0x501B</span></span>              |
| <span data-ttu-id="70d6c-1473">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1473">Type</span></span>  | <span data-ttu-id="70d6c-1474">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1474">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="70d6c-1475">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1475">Count</span></span> | <span data-ttu-id="70d6c-1476">變數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1476">Variable</span></span>            |



 

## <a name="propertytagthumbnailimagewidth"></a><span data-ttu-id="70d6c-1477">PropertyTagThumbnailImageWidth</span><span class="sxs-lookup"><span data-stu-id="70d6c-1477">PropertyTagThumbnailImageWidth</span></span>

<span data-ttu-id="70d6c-1478">縮圖影像中每個資料列的圖元數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1478">Number of pixels per row in the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1479">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1479">Property info</span></span> | <span data-ttu-id="70d6c-1480">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1480">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-1481">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1481">Tag</span></span>   | <span data-ttu-id="70d6c-1482">0x5020</span><span class="sxs-lookup"><span data-stu-id="70d6c-1482">0x5020</span></span>                                      |
| <span data-ttu-id="70d6c-1483">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1483">Type</span></span>  | <span data-ttu-id="70d6c-1484">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1484">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1485">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1485">Count</span></span> | <span data-ttu-id="70d6c-1486">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1486">1</span></span>                                           |



 

## <a name="propertytagthumbnailimageheight"></a><span data-ttu-id="70d6c-1487">PropertyTagThumbnailImageHeight</span><span class="sxs-lookup"><span data-stu-id="70d6c-1487">PropertyTagThumbnailImageHeight</span></span>

<span data-ttu-id="70d6c-1488">縮圖影像中的圖元資料列數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1488">Number of pixel rows in the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1489">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1489">Property info</span></span> | <span data-ttu-id="70d6c-1490">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1490">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-1491">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1491">Tag</span></span>   | <span data-ttu-id="70d6c-1492">0x5021</span><span class="sxs-lookup"><span data-stu-id="70d6c-1492">0x5021</span></span>                                      |
| <span data-ttu-id="70d6c-1493">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1493">Type</span></span>  | <span data-ttu-id="70d6c-1494">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1494">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1495">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1495">Count</span></span> | <span data-ttu-id="70d6c-1496">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1496">1</span></span>                                           |



 

## <a name="propertytagthumbnailbitspersample"></a><span data-ttu-id="70d6c-1497">PropertyTagThumbnailBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="70d6c-1497">PropertyTagThumbnailBitsPerSample</span></span>

<span data-ttu-id="70d6c-1498">縮圖影像中每個色彩元件的位數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1498">Number of bits per color component in the thumbnail image.</span></span> <span data-ttu-id="70d6c-1499">另請參閱 [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1499">See also [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span></span>



| <span data-ttu-id="70d6c-1500">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1500">Property info</span></span> | <span data-ttu-id="70d6c-1501">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1501">Value</span></span> |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="70d6c-1502">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1502">Tag</span></span>   | <span data-ttu-id="70d6c-1503">0x5022</span><span class="sxs-lookup"><span data-stu-id="70d6c-1503">0x5022</span></span>                                                          |
| <span data-ttu-id="70d6c-1504">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1504">Type</span></span>  | <span data-ttu-id="70d6c-1505">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1505">PropertyTagTypeShort</span></span>                                            |
| <span data-ttu-id="70d6c-1506">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1506">Count</span></span> | <span data-ttu-id="70d6c-1507">縮圖影像中每個圖元)  (元件的樣本數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1507">Number of samples (components) per pixel in the thumbnail image</span></span> |



 

## <a name="propertytagthumbnailcompression"></a><span data-ttu-id="70d6c-1508">PropertyTagThumbnailCompression</span><span class="sxs-lookup"><span data-stu-id="70d6c-1508">PropertyTagThumbnailCompression</span></span>

<span data-ttu-id="70d6c-1509">用於縮圖影像資料的壓縮配置。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1509">Compression scheme used for thumbnail image data.</span></span>



| <span data-ttu-id="70d6c-1510">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1510">Property info</span></span> | <span data-ttu-id="70d6c-1511">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1511">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1512">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1512">Tag</span></span>   | <span data-ttu-id="70d6c-1513">0x5023</span><span class="sxs-lookup"><span data-stu-id="70d6c-1513">0x5023</span></span>               |
| <span data-ttu-id="70d6c-1514">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1514">Type</span></span>  | <span data-ttu-id="70d6c-1515">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1515">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1516">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1516">Count</span></span> | <span data-ttu-id="70d6c-1517">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1517">1</span></span>                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a><span data-ttu-id="70d6c-1518">PropertyTagThumbnailPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="70d6c-1518">PropertyTagThumbnailPhotometricInterp</span></span>

<span data-ttu-id="70d6c-1519">縮圖圖元資料的轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1519">How thumbnail pixel data will be interpreted.</span></span>



| <span data-ttu-id="70d6c-1520">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1520">Property info</span></span> | <span data-ttu-id="70d6c-1521">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1521">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1522">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1522">Tag</span></span>   | <span data-ttu-id="70d6c-1523">0x5024</span><span class="sxs-lookup"><span data-stu-id="70d6c-1523">0x5024</span></span>               |
| <span data-ttu-id="70d6c-1524">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1524">Type</span></span>  | <span data-ttu-id="70d6c-1525">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1525">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1526">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1526">Count</span></span> | <span data-ttu-id="70d6c-1527">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1527">1</span></span>                    |



 

## <a name="propertytagthumbnailimagedescription"></a><span data-ttu-id="70d6c-1528">PropertyTagThumbnailImageDescription</span><span class="sxs-lookup"><span data-stu-id="70d6c-1528">PropertyTagThumbnailImageDescription</span></span>

<span data-ttu-id="70d6c-1529">以 Null 結束的字元字串，指定影像的標題。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1529">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="70d6c-1530">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1530">Property info</span></span> | <span data-ttu-id="70d6c-1531">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1531">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1532">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1532">Tag</span></span>   | <span data-ttu-id="70d6c-1533">0x5025</span><span class="sxs-lookup"><span data-stu-id="70d6c-1533">0x5025</span></span>                                             |
| <span data-ttu-id="70d6c-1534">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1534">Type</span></span>  | <span data-ttu-id="70d6c-1535">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1535">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1536">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1536">Count</span></span> | <span data-ttu-id="70d6c-1537">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1537">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmake"></a><span data-ttu-id="70d6c-1538">PropertyTagThumbnailEquipMake</span><span class="sxs-lookup"><span data-stu-id="70d6c-1538">PropertyTagThumbnailEquipMake</span></span>

<span data-ttu-id="70d6c-1539">以 Null 結束的字元字串，指定用來錄製縮圖影像的設備製造商。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1539">Null-terminated character string that specifies the manufacturer of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1540">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1540">Property info</span></span> | <span data-ttu-id="70d6c-1541">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1541">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1542">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1542">Tag</span></span>   | <span data-ttu-id="70d6c-1543">0x5026</span><span class="sxs-lookup"><span data-stu-id="70d6c-1543">0x5026</span></span>                                             |
| <span data-ttu-id="70d6c-1544">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1544">Type</span></span>  | <span data-ttu-id="70d6c-1545">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1545">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1546">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1546">Count</span></span> | <span data-ttu-id="70d6c-1547">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1547">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmodel"></a><span data-ttu-id="70d6c-1548">PropertyTagThumbnailEquipModel</span><span class="sxs-lookup"><span data-stu-id="70d6c-1548">PropertyTagThumbnailEquipModel</span></span>

<span data-ttu-id="70d6c-1549">以 Null 結束的字元字串，指定用來記錄縮圖影像之設備的模型名稱或模型編號。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1549">Null-terminated character string that specifies the model name or model number of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1550">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1550">Property info</span></span> | <span data-ttu-id="70d6c-1551">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1551">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1552">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1552">Tag</span></span>   | <span data-ttu-id="70d6c-1553">0x5027</span><span class="sxs-lookup"><span data-stu-id="70d6c-1553">0x5027</span></span>                                             |
| <span data-ttu-id="70d6c-1554">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1554">Type</span></span>  | <span data-ttu-id="70d6c-1555">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1555">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1556">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1556">Count</span></span> | <span data-ttu-id="70d6c-1557">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1557">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailstripoffsets"></a><span data-ttu-id="70d6c-1558">PropertyTagThumbnailStripOffsets</span><span class="sxs-lookup"><span data-stu-id="70d6c-1558">PropertyTagThumbnailStripOffsets</span></span>

<span data-ttu-id="70d6c-1559">縮圖影像中的每個區域，該區域的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1559">For each strip in the thumbnail image, the byte offset of that strip.</span></span> <span data-ttu-id="70d6c-1560">另請參閱 [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) 和 [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1560">See also [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) and [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span></span>



| <span data-ttu-id="70d6c-1561">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1561">Property info</span></span> | <span data-ttu-id="70d6c-1562">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1562">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-1563">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1563">Tag</span></span>   | <span data-ttu-id="70d6c-1564">0x5028</span><span class="sxs-lookup"><span data-stu-id="70d6c-1564">0x5028</span></span>                                      |
| <span data-ttu-id="70d6c-1565">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1565">Type</span></span>  | <span data-ttu-id="70d6c-1566">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1566">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1567">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1567">Count</span></span> | <span data-ttu-id="70d6c-1568">停車數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1568">Number of strips</span></span>                            |



 

## <a name="propertytagthumbnailorientation"></a><span data-ttu-id="70d6c-1569">PropertyTagThumbnailOrientation</span><span class="sxs-lookup"><span data-stu-id="70d6c-1569">PropertyTagThumbnailOrientation</span></span>

<span data-ttu-id="70d6c-1570">根據資料列和資料行的縮圖影像方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1570">Thumbnail image orientation in terms of rows and columns.</span></span> <span data-ttu-id="70d6c-1571">另請參閱 [PropertyTagOrientation](#propertytagorientation)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1571">See also [PropertyTagOrientation](#propertytagorientation).</span></span>



| <span data-ttu-id="70d6c-1572">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1572">Property info</span></span> | <span data-ttu-id="70d6c-1573">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1573">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1574">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1574">Tag</span></span>   | <span data-ttu-id="70d6c-1575">0x5029</span><span class="sxs-lookup"><span data-stu-id="70d6c-1575">0x5029</span></span>               |
| <span data-ttu-id="70d6c-1576">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1576">Type</span></span>  | <span data-ttu-id="70d6c-1577">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1577">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1578">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1578">Count</span></span> | <span data-ttu-id="70d6c-1579">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1579">1</span></span>                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a><span data-ttu-id="70d6c-1580">PropertyTagThumbnailSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="70d6c-1580">PropertyTagThumbnailSamplesPerPixel</span></span>

<span data-ttu-id="70d6c-1581">縮圖影像中每個圖元的色彩元件數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1581">Number of color components per pixel in the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1582">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1582">Property info</span></span> | <span data-ttu-id="70d6c-1583">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1583">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1584">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1584">Tag</span></span>   | <span data-ttu-id="70d6c-1585">0x502A</span><span class="sxs-lookup"><span data-stu-id="70d6c-1585">0x502A</span></span>               |
| <span data-ttu-id="70d6c-1586">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1586">Type</span></span>  | <span data-ttu-id="70d6c-1587">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1587">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1588">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1588">Count</span></span> | <span data-ttu-id="70d6c-1589">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1589">1</span></span>                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a><span data-ttu-id="70d6c-1590">PropertyTagThumbnailRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="70d6c-1590">PropertyTagThumbnailRowsPerStrip</span></span>

<span data-ttu-id="70d6c-1591">縮圖影像中每個資料列的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1591">Number of rows per strip in the thumbnail image.</span></span> <span data-ttu-id="70d6c-1592">另請參閱 [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) 和 [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1592">See also [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) and [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span></span>



| <span data-ttu-id="70d6c-1593">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1593">Property info</span></span> | <span data-ttu-id="70d6c-1594">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1594">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-1595">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1595">Tag</span></span>   | <span data-ttu-id="70d6c-1596">0x502B</span><span class="sxs-lookup"><span data-stu-id="70d6c-1596">0x502B</span></span>                                      |
| <span data-ttu-id="70d6c-1597">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1597">Type</span></span>  | <span data-ttu-id="70d6c-1598">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1598">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1599">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1599">Count</span></span> | <span data-ttu-id="70d6c-1600">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1600">1</span></span>                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a><span data-ttu-id="70d6c-1601">PropertyTagThumbnailStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="70d6c-1601">PropertyTagThumbnailStripBytesCount</span></span>

<span data-ttu-id="70d6c-1602">針對每個縮圖影像區域，該區域中的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1602">For each thumbnail image strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="70d6c-1603">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1603">Property info</span></span> | <span data-ttu-id="70d6c-1604">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1604">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-1605">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1605">Tag</span></span>   | <span data-ttu-id="70d6c-1606">0x502C</span><span class="sxs-lookup"><span data-stu-id="70d6c-1606">0x502C</span></span>                                      |
| <span data-ttu-id="70d6c-1607">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1607">Type</span></span>  | <span data-ttu-id="70d6c-1608">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1608">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1609">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1609">Count</span></span> | <span data-ttu-id="70d6c-1610">縮圖影像中的條紋數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1610">Number of strips in the thumbnail image</span></span>     |



 

## <a name="propertytagthumbnailresolutionx"></a><span data-ttu-id="70d6c-1611">PropertyTagThumbnailResolutionX</span><span class="sxs-lookup"><span data-stu-id="70d6c-1611">PropertyTagThumbnailResolutionX</span></span>

<span data-ttu-id="70d6c-1612">寬度方向的縮圖解析度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1612">Thumbnail resolution in the width direction.</span></span> <span data-ttu-id="70d6c-1613">解析單位會在 [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit)中提供。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1613">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="70d6c-1614">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1614">Property info</span></span> | <span data-ttu-id="70d6c-1615">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1615">Value</span></span> |
|-----|--------|
| <span data-ttu-id="70d6c-1616">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1616">Tag</span></span> | <span data-ttu-id="70d6c-1617">0x502D</span><span class="sxs-lookup"><span data-stu-id="70d6c-1617">0x502D</span></span> |



 

## <a name="propertytagthumbnailresolutiony"></a><span data-ttu-id="70d6c-1618">PropertyTagThumbnailResolutionY</span><span class="sxs-lookup"><span data-stu-id="70d6c-1618">PropertyTagThumbnailResolutionY</span></span>

<span data-ttu-id="70d6c-1619">高度方向的縮圖解析度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1619">Thumbnail resolution in the height direction.</span></span> <span data-ttu-id="70d6c-1620">解析單位會在 [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit)中提供。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1620">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="70d6c-1621">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1621">Property info</span></span> | <span data-ttu-id="70d6c-1622">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1622">Value</span></span> |
|-----|--------|
| <span data-ttu-id="70d6c-1623">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1623">Tag</span></span> | <span data-ttu-id="70d6c-1624">0x502E</span><span class="sxs-lookup"><span data-stu-id="70d6c-1624">0x502E</span></span> |



 

## <a name="propertytagthumbnailplanarconfig"></a><span data-ttu-id="70d6c-1625">PropertyTagThumbnailPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="70d6c-1625">PropertyTagThumbnailPlanarConfig</span></span>

<span data-ttu-id="70d6c-1626">縮圖影像中的圖元元件是否以大量或平面格式記錄。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1626">Whether pixel components in the thumbnail image are recorded in chunky or planar format.</span></span> <span data-ttu-id="70d6c-1627">另請參閱 [PropertyTagPlanarConfig](#propertytagplanarconfig)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1627">See also [PropertyTagPlanarConfig](#propertytagplanarconfig).</span></span>



| <span data-ttu-id="70d6c-1628">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1628">Property info</span></span> | <span data-ttu-id="70d6c-1629">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1629">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1630">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1630">Tag</span></span>   | <span data-ttu-id="70d6c-1631">0x502F</span><span class="sxs-lookup"><span data-stu-id="70d6c-1631">0x502F</span></span>               |
| <span data-ttu-id="70d6c-1632">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1632">Type</span></span>  | <span data-ttu-id="70d6c-1633">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1633">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1634">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1634">Count</span></span> | <span data-ttu-id="70d6c-1635">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1635">1</span></span>                    |



 

## <a name="propertytagthumbnailresolutionunit"></a><span data-ttu-id="70d6c-1636">PropertyTagThumbnailResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-1636">PropertyTagThumbnailResolutionUnit</span></span>

<span data-ttu-id="70d6c-1637">水準解析度的測量單位，以及縮圖影像的垂直解析度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1637">Unit of measure for the horizontal resolution and the vertical resolution of the thumbnail image.</span></span> <span data-ttu-id="70d6c-1638">另請參閱 [PropertyTagResolutionUnit](#propertytagresolutionunit)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1638">See also [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="70d6c-1639">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1639">Property info</span></span> | <span data-ttu-id="70d6c-1640">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1640">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1641">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1641">Tag</span></span>   | <span data-ttu-id="70d6c-1642">0x5030</span><span class="sxs-lookup"><span data-stu-id="70d6c-1642">0x5030</span></span>               |
| <span data-ttu-id="70d6c-1643">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1643">Type</span></span>  | <span data-ttu-id="70d6c-1644">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1644">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1645">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1645">Count</span></span> | <span data-ttu-id="70d6c-1646">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1646">1</span></span>                    |



 

## <a name="propertytagthumbnailtransferfunction"></a><span data-ttu-id="70d6c-1647">PropertyTagThumbnailTransferFunction</span><span class="sxs-lookup"><span data-stu-id="70d6c-1647">PropertyTagThumbnailTransferFunction</span></span>

<span data-ttu-id="70d6c-1648">為縮圖影像指定傳送函數的資料表。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1648">Tables that specify transfer functions for the thumbnail image.</span></span> <span data-ttu-id="70d6c-1649">另請參閱 [PropertyTagTransferFunction](#propertytagtransferfunction)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1649">See also [PropertyTagTransferFunction](#propertytagtransferfunction).</span></span>



| <span data-ttu-id="70d6c-1650">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1650">Property info</span></span> | <span data-ttu-id="70d6c-1651">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1651">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="70d6c-1652">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1652">Tag</span></span>   | <span data-ttu-id="70d6c-1653">0x5031</span><span class="sxs-lookup"><span data-stu-id="70d6c-1653">0x5031</span></span>                                               |
| <span data-ttu-id="70d6c-1654">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1654">Type</span></span>  | <span data-ttu-id="70d6c-1655">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1655">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="70d6c-1656">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1656">Count</span></span> | <span data-ttu-id="70d6c-1657">資料表所需的16位單字總數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1657">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagthumbnailsoftwareused"></a><span data-ttu-id="70d6c-1658">PropertyTagThumbnailSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="70d6c-1658">PropertyTagThumbnailSoftwareUsed</span></span>

<span data-ttu-id="70d6c-1659">以 Null 結束的字元字串，指定用來產生縮圖影像之裝置的軟體或固件的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1659">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1660">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1660">Property info</span></span> | <span data-ttu-id="70d6c-1661">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1661">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1662">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1662">Tag</span></span>   | <span data-ttu-id="70d6c-1663">0x5032</span><span class="sxs-lookup"><span data-stu-id="70d6c-1663">0x5032</span></span>                                             |
| <span data-ttu-id="70d6c-1664">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1664">Type</span></span>  | <span data-ttu-id="70d6c-1665">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1665">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1666">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1666">Count</span></span> | <span data-ttu-id="70d6c-1667">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1667">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnaildatetime"></a><span data-ttu-id="70d6c-1668">PropertyTagThumbnailDateTime</span><span class="sxs-lookup"><span data-stu-id="70d6c-1668">PropertyTagThumbnailDateTime</span></span>

<span data-ttu-id="70d6c-1669">建立縮圖影像的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1669">Date and time the thumbnail image was created.</span></span> <span data-ttu-id="70d6c-1670">另請參閱 [PropertyTagDateTime](#propertytagdatetime)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1670">See also [PropertyTagDateTime](#propertytagdatetime).</span></span>



| <span data-ttu-id="70d6c-1671">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1671">Property info</span></span> | <span data-ttu-id="70d6c-1672">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1672">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1673">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1673">Tag</span></span>   | <span data-ttu-id="70d6c-1674">0x5033</span><span class="sxs-lookup"><span data-stu-id="70d6c-1674">0x5033</span></span>               |
| <span data-ttu-id="70d6c-1675">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1675">Type</span></span>  | <span data-ttu-id="70d6c-1676">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1676">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="70d6c-1677">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1677">Count</span></span> | <span data-ttu-id="70d6c-1678">20</span><span class="sxs-lookup"><span data-stu-id="70d6c-1678">20</span></span>                   |



 

## <a name="propertytagthumbnailartist"></a><span data-ttu-id="70d6c-1679">PropertyTagThumbnailArtist</span><span class="sxs-lookup"><span data-stu-id="70d6c-1679">PropertyTagThumbnailArtist</span></span>

<span data-ttu-id="70d6c-1680">以 Null 結束的字元字串，指定建立縮圖影像的人員名稱。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1680">Null-terminated character string that specifies the name of the person who created the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1681">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1681">Property info</span></span> | <span data-ttu-id="70d6c-1682">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1682">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1683">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1683">Tag</span></span>   | <span data-ttu-id="70d6c-1684">0x5034</span><span class="sxs-lookup"><span data-stu-id="70d6c-1684">0x5034</span></span>                                             |
| <span data-ttu-id="70d6c-1685">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1685">Type</span></span>  | <span data-ttu-id="70d6c-1686">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1686">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1687">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1687">Count</span></span> | <span data-ttu-id="70d6c-1688">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1688">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailwhitepoint"></a><span data-ttu-id="70d6c-1689">PropertyTagThumbnailWhitePoint</span><span class="sxs-lookup"><span data-stu-id="70d6c-1689">PropertyTagThumbnailWhitePoint</span></span>

<span data-ttu-id="70d6c-1690">縮圖影像的白色點 Chromaticity。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1690">Chromaticity of the white point of the thumbnail image.</span></span> <span data-ttu-id="70d6c-1691">另請參閱 [PropertyTagWhitePoint](#propertytagwhitepoint)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1691">See also [PropertyTagWhitePoint](#propertytagwhitepoint).</span></span>



| <span data-ttu-id="70d6c-1692">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1692">Property info</span></span> | <span data-ttu-id="70d6c-1693">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1693">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1694">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1694">Tag</span></span>   | <span data-ttu-id="70d6c-1695">0x5035</span><span class="sxs-lookup"><span data-stu-id="70d6c-1695">0x5035</span></span>                  |
| <span data-ttu-id="70d6c-1696">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1696">Type</span></span>  | <span data-ttu-id="70d6c-1697">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1697">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1698">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1698">Count</span></span> | <span data-ttu-id="70d6c-1699">2</span><span class="sxs-lookup"><span data-stu-id="70d6c-1699">2</span></span>                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a><span data-ttu-id="70d6c-1700">PropertyTagThumbnailPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="70d6c-1700">PropertyTagThumbnailPrimaryChromaticities</span></span>

<span data-ttu-id="70d6c-1701">針對縮圖影像中的三種主要色彩，這是該色彩的 chromaticity。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1701">For each of the three primary colors in the thumbnail image, the chromaticity of that color.</span></span> <span data-ttu-id="70d6c-1702">另請參閱 [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1702">See also [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span></span>



| <span data-ttu-id="70d6c-1703">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1703">Property info</span></span> | <span data-ttu-id="70d6c-1704">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1704">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1705">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1705">Tag</span></span>   | <span data-ttu-id="70d6c-1706">0x5036</span><span class="sxs-lookup"><span data-stu-id="70d6c-1706">0x5036</span></span>                  |
| <span data-ttu-id="70d6c-1707">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1707">Type</span></span>  | <span data-ttu-id="70d6c-1708">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1708">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1709">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1709">Count</span></span> | <span data-ttu-id="70d6c-1710">6</span><span class="sxs-lookup"><span data-stu-id="70d6c-1710">6</span></span>                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a><span data-ttu-id="70d6c-1711">PropertyTagThumbnailYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="70d6c-1711">PropertyTagThumbnailYCbCrCoefficients</span></span>

<span data-ttu-id="70d6c-1712">從 RGB 轉換成 YCbCr 縮圖影像之資料的係數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1712">Coefficients for transformation from RGB to YCbCr data for the thumbnail image.</span></span> <span data-ttu-id="70d6c-1713">另請參閱 [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1713">See also [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span></span>



| <span data-ttu-id="70d6c-1714">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1714">Property info</span></span> | <span data-ttu-id="70d6c-1715">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1715">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1716">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1716">Tag</span></span>   | <span data-ttu-id="70d6c-1717">0x5037</span><span class="sxs-lookup"><span data-stu-id="70d6c-1717">0x5037</span></span>                  |
| <span data-ttu-id="70d6c-1718">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1718">Type</span></span>  | <span data-ttu-id="70d6c-1719">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1719">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1720">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1720">Count</span></span> | <span data-ttu-id="70d6c-1721">3</span><span class="sxs-lookup"><span data-stu-id="70d6c-1721">3</span></span>                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a><span data-ttu-id="70d6c-1722">PropertyTagThumbnailYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="70d6c-1722">PropertyTagThumbnailYCbCrSubsampling</span></span>

<span data-ttu-id="70d6c-1723">相對於縮圖影像的亮度元件，色度元件的取樣率。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1723">Sampling ratio of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="70d6c-1724">另請參閱 [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1724">See also [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span></span>



| <span data-ttu-id="70d6c-1725">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1725">Property info</span></span> | <span data-ttu-id="70d6c-1726">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1726">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1727">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1727">Tag</span></span>   | <span data-ttu-id="70d6c-1728">0x5038</span><span class="sxs-lookup"><span data-stu-id="70d6c-1728">0x5038</span></span>               |
| <span data-ttu-id="70d6c-1729">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1729">Type</span></span>  | <span data-ttu-id="70d6c-1730">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1730">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1731">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-1731">Count</span></span> | <span data-ttu-id="70d6c-1732">2</span><span class="sxs-lookup"><span data-stu-id="70d6c-1732">2</span></span>                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a><span data-ttu-id="70d6c-1733">PropertyTagThumbnailYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="70d6c-1733">PropertyTagThumbnailYCbCrPositioning</span></span>

<span data-ttu-id="70d6c-1734">色度元件相對於縮圖影像的亮度元件的位置。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1734">Position of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="70d6c-1735">另請參閱 [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1735">See also [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span></span>



| <span data-ttu-id="70d6c-1736">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1736">Property info</span></span> | <span data-ttu-id="70d6c-1737">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1737">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1738">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1738">Tag</span></span>   | <span data-ttu-id="70d6c-1739">0x5039</span><span class="sxs-lookup"><span data-stu-id="70d6c-1739">0x5039</span></span>               |
| <span data-ttu-id="70d6c-1740">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1740">Type</span></span>  | <span data-ttu-id="70d6c-1741">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1741">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1742">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1742">Count</span></span> | <span data-ttu-id="70d6c-1743">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1743">1</span></span>                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a><span data-ttu-id="70d6c-1744">PropertyTagThumbnailRefBlackWhite</span><span class="sxs-lookup"><span data-stu-id="70d6c-1744">PropertyTagThumbnailRefBlackWhite</span></span>

<span data-ttu-id="70d6c-1745">參考黑色點值以及縮圖影像的參考泛點值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1745">Reference black point value and reference white point value for the thumbnail image.</span></span> <span data-ttu-id="70d6c-1746">另請參閱 [PropertyTagREFBlackWhite](#propertytagrefblackwhite)。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1746">See also [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span></span>



| <span data-ttu-id="70d6c-1747">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1747">Property info</span></span> | <span data-ttu-id="70d6c-1748">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1748">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1749">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1749">Tag</span></span>   | <span data-ttu-id="70d6c-1750">0x503A</span><span class="sxs-lookup"><span data-stu-id="70d6c-1750">0x503A</span></span>                  |
| <span data-ttu-id="70d6c-1751">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1751">Type</span></span>  | <span data-ttu-id="70d6c-1752">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1752">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1753">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1753">Count</span></span> | <span data-ttu-id="70d6c-1754">6</span><span class="sxs-lookup"><span data-stu-id="70d6c-1754">6</span></span>                       |



 

## <a name="propertytagthumbnailcopyright"></a><span data-ttu-id="70d6c-1755">PropertyTagThumbnailCopyRight</span><span class="sxs-lookup"><span data-stu-id="70d6c-1755">PropertyTagThumbnailCopyRight</span></span>

<span data-ttu-id="70d6c-1756">以 Null 結束的字元字串，其中包含縮圖影像的著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1756">Null-terminated character string that contains copyright information for the thumbnail image.</span></span>



| <span data-ttu-id="70d6c-1757">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1757">Property info</span></span> | <span data-ttu-id="70d6c-1758">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1758">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1759">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1759">Tag</span></span>   | <span data-ttu-id="70d6c-1760">0x503B</span><span class="sxs-lookup"><span data-stu-id="70d6c-1760">0x503B</span></span>                                             |
| <span data-ttu-id="70d6c-1761">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1761">Type</span></span>  | <span data-ttu-id="70d6c-1762">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1762">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1763">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1763">Count</span></span> | <span data-ttu-id="70d6c-1764">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1764">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagluminancetable"></a><span data-ttu-id="70d6c-1765">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="70d6c-1765">PropertyTagLuminanceTable</span></span>

<span data-ttu-id="70d6c-1766">亮度表。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1766">Luminance table.</span></span> <span data-ttu-id="70d6c-1767">亮度表和色度資料表是用來控制 JPEG 品質。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1767">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="70d6c-1768">有效的亮度或色度資料表具有64型別 PropertyTagTypeShort 的專案。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1768">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="70d6c-1769">如果影像具有亮度資料表或色度資料表，則它必須有兩個數據表。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1769">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="70d6c-1770">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1770">Property info</span></span> | <span data-ttu-id="70d6c-1771">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1771">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1772">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1772">Tag</span></span>   | <span data-ttu-id="70d6c-1773">0x5090</span><span class="sxs-lookup"><span data-stu-id="70d6c-1773">0x5090</span></span>               |
| <span data-ttu-id="70d6c-1774">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1774">Type</span></span>  | <span data-ttu-id="70d6c-1775">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1775">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1776">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1776">Count</span></span> | <span data-ttu-id="70d6c-1777">64</span><span class="sxs-lookup"><span data-stu-id="70d6c-1777">64</span></span>                   |



 

## <a name="propertytagchrominancetable"></a><span data-ttu-id="70d6c-1778">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="70d6c-1778">PropertyTagChrominanceTable</span></span>

<span data-ttu-id="70d6c-1779">色度資料表。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1779">Chrominance table.</span></span> <span data-ttu-id="70d6c-1780">亮度表和色度資料表是用來控制 JPEG 品質。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1780">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="70d6c-1781">有效的亮度或色度資料表具有64型別 PropertyTagTypeShort 的專案。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1781">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="70d6c-1782">如果影像具有亮度資料表或色度資料表，則它必須有兩個數據表。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1782">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="70d6c-1783">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1783">Property info</span></span> | <span data-ttu-id="70d6c-1784">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1784">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1785">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1785">Tag</span></span>   | <span data-ttu-id="70d6c-1786">0x5091</span><span class="sxs-lookup"><span data-stu-id="70d6c-1786">0x5091</span></span>               |
| <span data-ttu-id="70d6c-1787">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1787">Type</span></span>  | <span data-ttu-id="70d6c-1788">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1788">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1789">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1789">Count</span></span> | <span data-ttu-id="70d6c-1790">64</span><span class="sxs-lookup"><span data-stu-id="70d6c-1790">64</span></span>                   |



 

## <a name="propertytagframedelay"></a><span data-ttu-id="70d6c-1791">PropertyTagFrameDelay</span><span class="sxs-lookup"><span data-stu-id="70d6c-1791">PropertyTagFrameDelay</span></span>

<span data-ttu-id="70d6c-1792">動畫 GIF 影像中兩個框架之間的時間延遲（百分之一秒）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1792">Time delay, in hundredths of a second, between two frames in an animated GIF image.</span></span>



| <span data-ttu-id="70d6c-1793">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1793">Property info</span></span> | <span data-ttu-id="70d6c-1794">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1794">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="70d6c-1795">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1795">Tag</span></span>   | <span data-ttu-id="70d6c-1796">0x5100</span><span class="sxs-lookup"><span data-stu-id="70d6c-1796">0x5100</span></span>                        |
| <span data-ttu-id="70d6c-1797">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1797">Type</span></span>  | <span data-ttu-id="70d6c-1798">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1798">PropertyTagTypeLong</span></span>           |
| <span data-ttu-id="70d6c-1799">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1799">Count</span></span> | <span data-ttu-id="70d6c-1800">影像中的畫面格數目</span><span class="sxs-lookup"><span data-stu-id="70d6c-1800">Number of frames in the image</span></span> |



 

## <a name="propertytagloopcount"></a><span data-ttu-id="70d6c-1801">PropertyTagLoopCount</span><span class="sxs-lookup"><span data-stu-id="70d6c-1801">PropertyTagLoopCount</span></span>

<span data-ttu-id="70d6c-1802">針對動畫 GIF 影像，顯示動畫的次數。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1802">For an animated GIF image, the number of times to display the animation.</span></span> <span data-ttu-id="70d6c-1803">值為0會指定動畫應無限顯示。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1803">A value of 0 specifies that the animation should be displayed infinitely.</span></span>



| <span data-ttu-id="70d6c-1804">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1804">Property info</span></span> | <span data-ttu-id="70d6c-1805">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1805">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1806">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1806">Tag</span></span>   | <span data-ttu-id="70d6c-1807">0x5101</span><span class="sxs-lookup"><span data-stu-id="70d6c-1807">0x5101</span></span>               |
| <span data-ttu-id="70d6c-1808">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1808">Type</span></span>  | <span data-ttu-id="70d6c-1809">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1809">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1810">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1810">Count</span></span> | <span data-ttu-id="70d6c-1811">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1811">1</span></span>                    |



 

## <a name="propertytagglobalpalette"></a><span data-ttu-id="70d6c-1812">PropertyTagGlobalPalette</span><span class="sxs-lookup"><span data-stu-id="70d6c-1812">PropertyTagGlobalPalette</span></span>

<span data-ttu-id="70d6c-1813">GIF 影像中索引點陣圖的色調色板。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1813">Color palette for an indexed bitmap in a GIF image.</span></span>



| <span data-ttu-id="70d6c-1814">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1814">Property info</span></span> | <span data-ttu-id="70d6c-1815">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1815">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="70d6c-1816">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1816">Tag</span></span>   | <span data-ttu-id="70d6c-1817">0x5102</span><span class="sxs-lookup"><span data-stu-id="70d6c-1817">0x5102</span></span>                        |
| <span data-ttu-id="70d6c-1818">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1818">Type</span></span>  | <span data-ttu-id="70d6c-1819">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1819">PropertyTagTypeByte</span></span>           |
| <span data-ttu-id="70d6c-1820">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1820">Count</span></span> | <span data-ttu-id="70d6c-1821">3 x 個調色板專案數目</span><span class="sxs-lookup"><span data-stu-id="70d6c-1821">3 x number of palette entries</span></span> |



 

## <a name="propertytagindexbackground"></a><span data-ttu-id="70d6c-1822">PropertyTagIndexBackground</span><span class="sxs-lookup"><span data-stu-id="70d6c-1822">PropertyTagIndexBackground</span></span>

<span data-ttu-id="70d6c-1823">GIF 影像之調色板中的背景色彩索引。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1823">Index of the background color in the palette of a GIF image.</span></span>



| <span data-ttu-id="70d6c-1824">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1824">Property info</span></span> | <span data-ttu-id="70d6c-1825">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1825">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1826">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1826">Tag</span></span>   | <span data-ttu-id="70d6c-1827">0x5103</span><span class="sxs-lookup"><span data-stu-id="70d6c-1827">0x5103</span></span>              |
| <span data-ttu-id="70d6c-1828">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1828">Type</span></span>  | <span data-ttu-id="70d6c-1829">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1829">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="70d6c-1830">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1830">Count</span></span> | <span data-ttu-id="70d6c-1831">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1831">1</span></span>                   |



 

## <a name="propertytagindextransparent"></a><span data-ttu-id="70d6c-1832">PropertyTagIndexTransparent</span><span class="sxs-lookup"><span data-stu-id="70d6c-1832">PropertyTagIndexTransparent</span></span>

<span data-ttu-id="70d6c-1833">GIF 影像的調色板中透明色彩的索引。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1833">Index of the transparent color in the palette of a GIF image.</span></span>



| <span data-ttu-id="70d6c-1834">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1834">Property info</span></span> | <span data-ttu-id="70d6c-1835">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1835">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1836">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1836">Tag</span></span>   | <span data-ttu-id="70d6c-1837">0x5104</span><span class="sxs-lookup"><span data-stu-id="70d6c-1837">0x5104</span></span>              |
| <span data-ttu-id="70d6c-1838">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1838">Type</span></span>  | <span data-ttu-id="70d6c-1839">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1839">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="70d6c-1840">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1840">Count</span></span> | <span data-ttu-id="70d6c-1841">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1841">1</span></span>                   |



 

## <a name="propertytagpixelunit"></a><span data-ttu-id="70d6c-1842">PropertyTagPixelUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-1842">PropertyTagPixelUnit</span></span>

<span data-ttu-id="70d6c-1843">PropertyTagPixelPerUnitX 和 PropertyTagPixelPerUnitY 的單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1843">Unit for PropertyTagPixelPerUnitX and PropertyTagPixelPerUnitY.</span></span>



<span data-ttu-id="70d6c-1844">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1844">Tag</span></span>

<span data-ttu-id="70d6c-1845">0x5110</span><span class="sxs-lookup"><span data-stu-id="70d6c-1845">0x5110</span></span>

<span data-ttu-id="70d6c-1846">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1846">Type</span></span>

<span data-ttu-id="70d6c-1847">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1847">PropertyTagTypeByte</span></span>

<span data-ttu-id="70d6c-1848">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1848">Count</span></span>

<span data-ttu-id="70d6c-1849">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1849">1</span></span>

<span data-ttu-id="70d6c-1850">0-未知</span><span class="sxs-lookup"><span data-stu-id="70d6c-1850">0 - unknown</span></span>



 

## <a name="propertytagpixelperunitx"></a><span data-ttu-id="70d6c-1851">PropertyTagPixelPerUnitX</span><span class="sxs-lookup"><span data-stu-id="70d6c-1851">PropertyTagPixelPerUnitX</span></span>

<span data-ttu-id="70d6c-1852">X 方向的每單位圖元。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1852">Pixels per unit in the x direction.</span></span>



| <span data-ttu-id="70d6c-1853">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1853">Property info</span></span> | <span data-ttu-id="70d6c-1854">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1854">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1855">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1855">Tag</span></span>   | <span data-ttu-id="70d6c-1856">0x5111</span><span class="sxs-lookup"><span data-stu-id="70d6c-1856">0x5111</span></span>              |
| <span data-ttu-id="70d6c-1857">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1857">Type</span></span>  | <span data-ttu-id="70d6c-1858">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1858">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1859">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1859">Count</span></span> | <span data-ttu-id="70d6c-1860">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1860">1</span></span>                   |



 

## <a name="propertytagpixelperunity"></a><span data-ttu-id="70d6c-1861">PropertyTagPixelPerUnitY</span><span class="sxs-lookup"><span data-stu-id="70d6c-1861">PropertyTagPixelPerUnitY</span></span>

<span data-ttu-id="70d6c-1862">Y 方向的每單位圖元。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1862">Pixels per unit in the y direction.</span></span>



| <span data-ttu-id="70d6c-1863">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1863">Property info</span></span> | <span data-ttu-id="70d6c-1864">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1864">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1865">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1865">Tag</span></span>   | <span data-ttu-id="70d6c-1866">0x5112</span><span class="sxs-lookup"><span data-stu-id="70d6c-1866">0x5112</span></span>              |
| <span data-ttu-id="70d6c-1867">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1867">Type</span></span>  | <span data-ttu-id="70d6c-1868">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1868">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1869">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1869">Count</span></span> | <span data-ttu-id="70d6c-1870">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1870">1</span></span>                   |



 

## <a name="propertytagpalettehistogram"></a><span data-ttu-id="70d6c-1871">PropertyTagPaletteHistogram</span><span class="sxs-lookup"><span data-stu-id="70d6c-1871">PropertyTagPaletteHistogram</span></span>

<span data-ttu-id="70d6c-1872">調色板長條圖。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1872">Palette histogram.</span></span>



| <span data-ttu-id="70d6c-1873">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1873">Property info</span></span> | <span data-ttu-id="70d6c-1874">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1874">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1875">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1875">Tag</span></span>   | <span data-ttu-id="70d6c-1876">0x5113</span><span class="sxs-lookup"><span data-stu-id="70d6c-1876">0x5113</span></span>                  |
| <span data-ttu-id="70d6c-1877">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1877">Type</span></span>  | <span data-ttu-id="70d6c-1878">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1878">PropertyTagTypeByte</span></span>     |
| <span data-ttu-id="70d6c-1879">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1879">Count</span></span> | <span data-ttu-id="70d6c-1880">長條圖的長度</span><span class="sxs-lookup"><span data-stu-id="70d6c-1880">Length of the histogram</span></span> |



 

## <a name="propertytagcopyright"></a><span data-ttu-id="70d6c-1881">PropertyTagCopyright</span><span class="sxs-lookup"><span data-stu-id="70d6c-1881">PropertyTagCopyright</span></span>

<span data-ttu-id="70d6c-1882">以 Null 結束的字元字串，其中包含著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1882">Null-terminated character string that contains copyright information.</span></span>



| <span data-ttu-id="70d6c-1883">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1883">Property info</span></span> | <span data-ttu-id="70d6c-1884">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1884">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1885">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1885">Tag</span></span>   | <span data-ttu-id="70d6c-1886">0x8298</span><span class="sxs-lookup"><span data-stu-id="70d6c-1886">0x8298</span></span>                                             |
| <span data-ttu-id="70d6c-1887">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1887">Type</span></span>  | <span data-ttu-id="70d6c-1888">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1888">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1889">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1889">Count</span></span> | <span data-ttu-id="70d6c-1890">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1890">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifexposuretime"></a><span data-ttu-id="70d6c-1891">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="70d6c-1891">PropertyTagExifExposureTime</span></span>

<span data-ttu-id="70d6c-1892">曝光時間，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1892">Exposure time, measured in seconds.</span></span>



| <span data-ttu-id="70d6c-1893">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1893">Property info</span></span> | <span data-ttu-id="70d6c-1894">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1894">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-1895">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1895">Tag</span></span>   | <span data-ttu-id="70d6c-1896">0x829A</span><span class="sxs-lookup"><span data-stu-id="70d6c-1896">0x829A</span></span>                  |
| <span data-ttu-id="70d6c-1897">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1897">Type</span></span>  | <span data-ttu-id="70d6c-1898">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-1898">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-1899">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1899">Count</span></span> | <span data-ttu-id="70d6c-1900">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1900">1</span></span>                       |



 

## <a name="propertytagexiffnumber"></a><span data-ttu-id="70d6c-1901">PropertyTagExifFNumber</span><span class="sxs-lookup"><span data-stu-id="70d6c-1901">PropertyTagExifFNumber</span></span>

<span data-ttu-id="70d6c-1902">F 編號。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1902">F number.</span></span>



| <span data-ttu-id="70d6c-1903">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1903">Property info</span></span> | <span data-ttu-id="70d6c-1904">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1904">Value</span></span> |
|-------|----------|
| <span data-ttu-id="70d6c-1905">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1905">Tag</span></span>   | <span data-ttu-id="70d6c-1906">0x829D</span><span class="sxs-lookup"><span data-stu-id="70d6c-1906">0x829D</span></span>   |
| <span data-ttu-id="70d6c-1907">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1907">Type</span></span>  | <span data-ttu-id="70d6c-1908">理性</span><span class="sxs-lookup"><span data-stu-id="70d6c-1908">RATIONAL</span></span> |
| <span data-ttu-id="70d6c-1909">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1909">Count</span></span> | <span data-ttu-id="70d6c-1910">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1910">1</span></span>        |



 

## <a name="propertytagexififd"></a><span data-ttu-id="70d6c-1911">PropertyTagExifIFD</span><span class="sxs-lookup"><span data-stu-id="70d6c-1911">PropertyTagExifIFD</span></span>

<span data-ttu-id="70d6c-1912">GDI + 所使用的私用標記。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1912">Private tag used by GDI+.</span></span> <span data-ttu-id="70d6c-1913">不提供公開使用。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1913">Not for public use.</span></span> <span data-ttu-id="70d6c-1914">GDI + 會使用這個標記來尋找 Exif 特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1914">GDI+ uses this tag to locate Exif-specific information.</span></span>



| <span data-ttu-id="70d6c-1915">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1915">Property info</span></span> | <span data-ttu-id="70d6c-1916">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1916">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1917">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1917">Tag</span></span>   | <span data-ttu-id="70d6c-1918">0x8769</span><span class="sxs-lookup"><span data-stu-id="70d6c-1918">0x8769</span></span>              |
| <span data-ttu-id="70d6c-1919">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1919">Type</span></span>  | <span data-ttu-id="70d6c-1920">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1920">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1921">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1921">Count</span></span> | <span data-ttu-id="70d6c-1922">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1922">1</span></span>                   |



 

## <a name="propertytagiccprofile"></a><span data-ttu-id="70d6c-1923">PropertyTagICCProfile</span><span class="sxs-lookup"><span data-stu-id="70d6c-1923">PropertyTagICCProfile</span></span>

<span data-ttu-id="70d6c-1924">內嵌于映射中的 ICC 設定檔。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1924">ICC profile embedded in the image.</span></span>



| <span data-ttu-id="70d6c-1925">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1925">Property info</span></span> | <span data-ttu-id="70d6c-1926">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1926">Value</span></span> |
|-------|-----------------------|
| <span data-ttu-id="70d6c-1927">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1927">Tag</span></span>   | <span data-ttu-id="70d6c-1928">0x8773</span><span class="sxs-lookup"><span data-stu-id="70d6c-1928">0x8773</span></span>                |
| <span data-ttu-id="70d6c-1929">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1929">Type</span></span>  | <span data-ttu-id="70d6c-1930">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="70d6c-1930">PropertyTagTypeByte</span></span>   |
| <span data-ttu-id="70d6c-1931">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1931">Count</span></span> | <span data-ttu-id="70d6c-1932">設定檔的長度</span><span class="sxs-lookup"><span data-stu-id="70d6c-1932">Length of the profile</span></span> |



 

## <a name="propertytagexifexposureprog"></a><span data-ttu-id="70d6c-1933">PropertyTagExifExposureProg</span><span class="sxs-lookup"><span data-stu-id="70d6c-1933">PropertyTagExifExposureProg</span></span>

<span data-ttu-id="70d6c-1934">相機使用的程式類別，在拍攝圖片時設定曝光。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1934">Class of the program used by the camera to set exposure when the picture is taken.</span></span>



<span data-ttu-id="70d6c-1935">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1935">Tag</span></span>

<span data-ttu-id="70d6c-1936">0x8822</span><span class="sxs-lookup"><span data-stu-id="70d6c-1936">0x8822</span></span>

<span data-ttu-id="70d6c-1937">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1937">Type</span></span>

<span data-ttu-id="70d6c-1938">SHORT</span><span class="sxs-lookup"><span data-stu-id="70d6c-1938">SHORT</span></span>

<span data-ttu-id="70d6c-1939">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1939">Count</span></span>

<span data-ttu-id="70d6c-1940">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1940">1</span></span>

<span data-ttu-id="70d6c-1941">預設</span><span class="sxs-lookup"><span data-stu-id="70d6c-1941">Default</span></span>

<span data-ttu-id="70d6c-1942">0</span><span class="sxs-lookup"><span data-stu-id="70d6c-1942">0</span></span>

<span data-ttu-id="70d6c-1943">0-未定義 1-手動 2-一般程式 3-光圈先決級 4-快門優先 5-創意計畫 (偏高) 6-行動計畫 (偏高的快門速度) 7-縱向模式 (適用于具有背景焦點的橫向相片) 9 至 255-保留</span><span class="sxs-lookup"><span data-stu-id="70d6c-1943">0 - not defined 1 - manual 2 - normal program 3 - aperture priority 4 - shutter priority 5 - creative program (biased toward depth of field) 6 - action program (biased toward fast shutter speed) 7 - portrait mode (for close-up photos with the background out of focus) 8 - landscape mode (for landscape photos with the background in focus) 9 to 255 - reserved</span></span>



 

## <a name="propertytagexifspectralsense"></a><span data-ttu-id="70d6c-1944">PropertyTagExifSpectralSense</span><span class="sxs-lookup"><span data-stu-id="70d6c-1944">PropertyTagExifSpectralSense</span></span>

<span data-ttu-id="70d6c-1945">以 Null 結束的字元字串，指定所使用之相機的每個通道的光譜敏感度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1945">Null-terminated character string that specifies the spectral sensitivity of each channel of the camera used.</span></span> <span data-ttu-id="70d6c-1946">此字串與 ASTM 技術委員會所開發的標準相容。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1946">The string is compatible with the standard developed by the ASTM Technical Committee.</span></span>



| <span data-ttu-id="70d6c-1947">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1947">Property info</span></span> | <span data-ttu-id="70d6c-1948">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1948">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-1949">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1949">Tag</span></span>   | <span data-ttu-id="70d6c-1950">0x8824</span><span class="sxs-lookup"><span data-stu-id="70d6c-1950">0x8824</span></span>                                             |
| <span data-ttu-id="70d6c-1951">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1951">Type</span></span>  | <span data-ttu-id="70d6c-1952">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-1952">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-1953">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1953">Count</span></span> | <span data-ttu-id="70d6c-1954">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-1954">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsifd"></a><span data-ttu-id="70d6c-1955">PropertyTagGpsIFD</span><span class="sxs-lookup"><span data-stu-id="70d6c-1955">PropertyTagGpsIFD</span></span>

<span data-ttu-id="70d6c-1956">GPS 屬性專案區塊的位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1956">Offset to a block of GPS property items.</span></span> <span data-ttu-id="70d6c-1957">其標記具有前置詞 PropertyTagGps 的屬性專案會儲存在 GPS 區塊中。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1957">Property items whose tags have the prefix PropertyTagGps are stored in the GPS block.</span></span> <span data-ttu-id="70d6c-1958">GPS 屬性專案是在 EXIF 規格中定義。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1958">The GPS property items are defined in the EXIF specification.</span></span> <span data-ttu-id="70d6c-1959">GDI + 會使用這個標記來找出 GPS 資訊，但 GDI + 不會公開此標記以供公開使用。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1959">GDI+ uses this tag to locate GPS information, but GDI+ does not expose this tag for public use.</span></span>



| <span data-ttu-id="70d6c-1960">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1960">Property info</span></span> | <span data-ttu-id="70d6c-1961">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1961">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-1962">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1962">Tag</span></span>   | <span data-ttu-id="70d6c-1963">0x8825</span><span class="sxs-lookup"><span data-stu-id="70d6c-1963">0x8825</span></span>              |
| <span data-ttu-id="70d6c-1964">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1964">Type</span></span>  | <span data-ttu-id="70d6c-1965">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-1965">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-1966">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1966">Count</span></span> | <span data-ttu-id="70d6c-1967">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-1967">1</span></span>                   |



 

## <a name="propertytagexifisospeed"></a><span data-ttu-id="70d6c-1968">PropertyTagExifISOSpeed</span><span class="sxs-lookup"><span data-stu-id="70d6c-1968">PropertyTagExifISOSpeed</span></span>

<span data-ttu-id="70d6c-1969">以 iso 12232 指定的相機或輸入裝置的 ISO 速度和 ISO 緯度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1969">ISO speed and ISO latitude of the camera or input device as specified in ISO 12232.</span></span>



| <span data-ttu-id="70d6c-1970">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1970">Property info</span></span> | <span data-ttu-id="70d6c-1971">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1971">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-1972">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1972">Tag</span></span>   | <span data-ttu-id="70d6c-1973">0x8827</span><span class="sxs-lookup"><span data-stu-id="70d6c-1973">0x8827</span></span>               |
| <span data-ttu-id="70d6c-1974">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1974">Type</span></span>  | <span data-ttu-id="70d6c-1975">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-1975">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-1976">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1976">Count</span></span> | <span data-ttu-id="70d6c-1977">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-1977">Any</span></span>                  |



 

## <a name="propertytagexifoecf"></a><span data-ttu-id="70d6c-1978">PropertyTagExifOECF</span><span class="sxs-lookup"><span data-stu-id="70d6c-1978">PropertyTagExifOECF</span></span>

<span data-ttu-id="70d6c-1979">Optoelectronic 轉換函式 (ISO 14524 中指定的 OECF) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1979">Optoelectronic conversion function (OECF) specified in ISO 14524.</span></span> <span data-ttu-id="70d6c-1980">OECF 是攝影機光學輸入與影像值之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1980">The OECF is the relationship between the camera optical input and the image values.</span></span>



| <span data-ttu-id="70d6c-1981">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1981">Property info</span></span> | <span data-ttu-id="70d6c-1982">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1982">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-1983">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1983">Tag</span></span>   | <span data-ttu-id="70d6c-1984">0x8828</span><span class="sxs-lookup"><span data-stu-id="70d6c-1984">0x8828</span></span>                   |
| <span data-ttu-id="70d6c-1985">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1985">Type</span></span>  | <span data-ttu-id="70d6c-1986">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-1986">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-1987">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-1987">Count</span></span> | <span data-ttu-id="70d6c-1988">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-1988">Any</span></span>                      |



 

## <a name="propertytagexifver"></a><span data-ttu-id="70d6c-1989">PropertyTagExifVer</span><span class="sxs-lookup"><span data-stu-id="70d6c-1989">PropertyTagExifVer</span></span>

<span data-ttu-id="70d6c-1990">支援的 EXIF 標準版本。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1990">Version of the EXIF standard supported.</span></span> <span data-ttu-id="70d6c-1991">此欄位的存在會用來表示標準的不符合項。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1991">Nonexistence of this field is taken to mean nonconformance to the standard.</span></span> <span data-ttu-id="70d6c-1992">將0210記錄為4位元組 ASCII 字串表示標準的一致性。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1992">Conformance to the standard is indicated by recording 0210 as a 4-byte ASCII string.</span></span> <span data-ttu-id="70d6c-1993">因為類型是 PropertyTagTypeUndefined，所以沒有 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="70d6c-1993">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



| <span data-ttu-id="70d6c-1994">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-1994">Property info</span></span> | <span data-ttu-id="70d6c-1995">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-1995">Value</span></span> |
|---------|--------------------------|
| <span data-ttu-id="70d6c-1996">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-1996">Tag</span></span>     | <span data-ttu-id="70d6c-1997">0x9000</span><span class="sxs-lookup"><span data-stu-id="70d6c-1997">0x9000</span></span>                   |
| <span data-ttu-id="70d6c-1998">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-1998">Type</span></span>    | <span data-ttu-id="70d6c-1999">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-1999">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-2000">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2000">Count</span></span>   | <span data-ttu-id="70d6c-2001">4</span><span class="sxs-lookup"><span data-stu-id="70d6c-2001">4</span></span>                        |
| <span data-ttu-id="70d6c-2002">預設</span><span class="sxs-lookup"><span data-stu-id="70d6c-2002">Default</span></span> | <span data-ttu-id="70d6c-2003">0210</span><span class="sxs-lookup"><span data-stu-id="70d6c-2003">0210</span></span>                     |



 

## <a name="propertytagexifdtorig"></a><span data-ttu-id="70d6c-2004">PropertyTagExifDTOrig</span><span class="sxs-lookup"><span data-stu-id="70d6c-2004">PropertyTagExifDTOrig</span></span>

<span data-ttu-id="70d6c-2005">產生原始影像資料的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2005">Date and time when the original image data was generated.</span></span> <span data-ttu-id="70d6c-2006">DSC 是拍攝圖片的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2006">For a DSC, the date and time when the picture was taken.</span></span> <span data-ttu-id="70d6c-2007">格式為 YYYY： MM： DD HH： MM： SS，以24小時制顯示時間，並以一個空白字元分隔日期和時間 (0x2000) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2007">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="70d6c-2008">字元字串長度為20個位元組，包括 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2008">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="70d6c-2009">當欄位為空白時，就會將其視為未知。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2009">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="70d6c-2010">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2010">Property info</span></span> | <span data-ttu-id="70d6c-2011">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2011">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-2012">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2012">Tag</span></span>   | <span data-ttu-id="70d6c-2013">0x9003</span><span class="sxs-lookup"><span data-stu-id="70d6c-2013">0x9003</span></span>               |
| <span data-ttu-id="70d6c-2014">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2014">Type</span></span>  | <span data-ttu-id="70d6c-2015">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-2015">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="70d6c-2016">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2016">Count</span></span> | <span data-ttu-id="70d6c-2017">20</span><span class="sxs-lookup"><span data-stu-id="70d6c-2017">20</span></span>                   |



 

## <a name="propertytagexifdtdigitized"></a><span data-ttu-id="70d6c-2018">PropertyTagExifDTDigitized</span><span class="sxs-lookup"><span data-stu-id="70d6c-2018">PropertyTagExifDTDigitized</span></span>

<span data-ttu-id="70d6c-2019">影像儲存為數字資料的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2019">Date and time when the image was stored as digital data.</span></span> <span data-ttu-id="70d6c-2020">例如，如果影像是由 DSC 所捕捉，並且在記錄檔的同時，則 DateTimeOriginal 和 DateTimeDigitized 將會有相同的內容。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2020">If, for example, an image was captured by DSC and at the same time the file was recorded, then DateTimeOriginal and DateTimeDigitized will have the same contents.</span></span>

<span data-ttu-id="70d6c-2021">格式為 YYYY： MM： DD HH： MM： SS，以24小時制顯示時間，並以一個空白字元分隔日期和時間 (0x2000) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2021">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="70d6c-2022">字元字串長度為20個位元組，包括 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2022">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="70d6c-2023">當欄位為空白時，就會將其視為未知。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2023">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="70d6c-2024">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2024">Property info</span></span> | <span data-ttu-id="70d6c-2025">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2025">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-2026">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2026">Tag</span></span>   | <span data-ttu-id="70d6c-2027">0x9004</span><span class="sxs-lookup"><span data-stu-id="70d6c-2027">0x9004</span></span>               |
| <span data-ttu-id="70d6c-2028">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2028">Type</span></span>  | <span data-ttu-id="70d6c-2029">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-2029">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="70d6c-2030">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2030">Count</span></span> | <span data-ttu-id="70d6c-2031">20</span><span class="sxs-lookup"><span data-stu-id="70d6c-2031">20</span></span>                   |



 

## <a name="propertytagexifcompconfig"></a><span data-ttu-id="70d6c-2032">PropertyTagExifCompConfig</span><span class="sxs-lookup"><span data-stu-id="70d6c-2032">PropertyTagExifCompConfig</span></span>

<span data-ttu-id="70d6c-2033">壓縮資料的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2033">Information specific to compressed data.</span></span> <span data-ttu-id="70d6c-2034">每個元件的通道會依序從第一個元件排列至第四個元件。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2034">The channels of each component are arranged in order from the first component to the fourth.</span></span> <span data-ttu-id="70d6c-2035">針對未壓縮的資料，PropertyTagPhotometricInterp 標記中會提供資料排列。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2035">For uncompressed data, the data arrangement is given in the PropertyTagPhotometricInterp tag.</span></span>

<span data-ttu-id="70d6c-2036">不過，因為 PropertyTagPhotometricInterp 只能表達 Y、Cb 和 Cr 的順序，所以當壓縮的資料使用 Y、Cb 和 Cr 以外的元件，並支援其他順序時，就會提供此標記。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2036">However, because PropertyTagPhotometricInterp can only express the order of Y, Cb, and Cr, this tag is provided for cases when compressed data uses components other than Y, Cb, and Cr and to support other sequences.</span></span>



<span data-ttu-id="70d6c-2037">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2037">Tag</span></span>

<span data-ttu-id="70d6c-2038">0x9101</span><span class="sxs-lookup"><span data-stu-id="70d6c-2038">0x9101</span></span>

<span data-ttu-id="70d6c-2039">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2039">Type</span></span>

<span data-ttu-id="70d6c-2040">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-2040">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="70d6c-2041">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2041">Count</span></span>

<span data-ttu-id="70d6c-2042">4</span><span class="sxs-lookup"><span data-stu-id="70d6c-2042">4</span></span>

<span data-ttu-id="70d6c-2043">預設</span><span class="sxs-lookup"><span data-stu-id="70d6c-2043">Default</span></span>

<span data-ttu-id="70d6c-2044">4 5 6 0 (如果 RGB 未壓縮) 1 2 3 0 (其他案例) </span><span class="sxs-lookup"><span data-stu-id="70d6c-2044">4 5 6 0 (if RGB uncompressed) 1 2 3 0 (other cases)</span></span>

<span data-ttu-id="70d6c-2045">0-不存在 1-Y 2-Cb 3-Cr 4-R 5-G 6-B （其他）保留</span><span class="sxs-lookup"><span data-stu-id="70d6c-2045">0 - does not exist 1 - Y 2 - Cb 3 - Cr 4 - R 5 - G 6 - B Other - reserved</span></span>



 

## <a name="propertytagexifcompbpp"></a><span data-ttu-id="70d6c-2046">PropertyTagExifCompBPP</span><span class="sxs-lookup"><span data-stu-id="70d6c-2046">PropertyTagExifCompBPP</span></span>

<span data-ttu-id="70d6c-2047">壓縮資料的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2047">Information specific to compressed data.</span></span> <span data-ttu-id="70d6c-2048">壓縮的影像所使用的壓縮模式會以單位 BPP 表示。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2048">The compression mode used for a compressed image is indicated in unit BPP.</span></span>



| <span data-ttu-id="70d6c-2049">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2049">Property info</span></span> | <span data-ttu-id="70d6c-2050">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2050">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2051">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2051">Tag</span></span>   | <span data-ttu-id="70d6c-2052">0x9102</span><span class="sxs-lookup"><span data-stu-id="70d6c-2052">0x9102</span></span>                  |
| <span data-ttu-id="70d6c-2053">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2053">Type</span></span>  | <span data-ttu-id="70d6c-2054">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2054">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2055">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2055">Count</span></span> | <span data-ttu-id="70d6c-2056">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2056">1</span></span>                       |



 

## <a name="propertytagexifshutterspeed"></a><span data-ttu-id="70d6c-2057">PropertyTagExifShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="70d6c-2057">PropertyTagExifShutterSpeed</span></span>

<span data-ttu-id="70d6c-2058">快門速度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2058">Shutter speed.</span></span> <span data-ttu-id="70d6c-2059">此單位是影像曝光的加法系統 (頂點) 值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2059">The unit is the Additive System of Photographic Exposure (APEX) value.</span></span>



| <span data-ttu-id="70d6c-2060">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2060">Property info</span></span> | <span data-ttu-id="70d6c-2061">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2061">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2062">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2062">Tag</span></span>   | <span data-ttu-id="70d6c-2063">0x9201</span><span class="sxs-lookup"><span data-stu-id="70d6c-2063">0x9201</span></span>                   |
| <span data-ttu-id="70d6c-2064">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2064">Type</span></span>  | <span data-ttu-id="70d6c-2065">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2065">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="70d6c-2066">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2066">Count</span></span> | <span data-ttu-id="70d6c-2067">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2067">1</span></span>                        |



 

## <a name="propertytagexifaperture"></a><span data-ttu-id="70d6c-2068">PropertyTagExifAperture</span><span class="sxs-lookup"><span data-stu-id="70d6c-2068">PropertyTagExifAperture</span></span>

<span data-ttu-id="70d6c-2069">鏡頭光圈。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2069">Lens aperture.</span></span> <span data-ttu-id="70d6c-2070">此單位為頂點值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2070">The unit is the APEX value.</span></span>



| <span data-ttu-id="70d6c-2071">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2071">Property info</span></span> | <span data-ttu-id="70d6c-2072">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2072">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2073">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2073">Tag</span></span>   | <span data-ttu-id="70d6c-2074">0x9202</span><span class="sxs-lookup"><span data-stu-id="70d6c-2074">0x9202</span></span>                  |
| <span data-ttu-id="70d6c-2075">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2075">Type</span></span>  | <span data-ttu-id="70d6c-2076">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2076">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2077">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2077">Count</span></span> | <span data-ttu-id="70d6c-2078">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2078">1</span></span>                       |



 

## <a name="propertytagexifbrightness"></a><span data-ttu-id="70d6c-2079">PropertyTagExifBrightness</span><span class="sxs-lookup"><span data-stu-id="70d6c-2079">PropertyTagExifBrightness</span></span>

<span data-ttu-id="70d6c-2080">亮度值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2080">Brightness value.</span></span> <span data-ttu-id="70d6c-2081">此單位為頂點值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2081">The unit is the APEX value.</span></span> <span data-ttu-id="70d6c-2082">通常會在-99.99 到99.99 的範圍中提供。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2082">Ordinarily it is given in the range of -99.99 to 99.99.</span></span>



| <span data-ttu-id="70d6c-2083">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2083">Property info</span></span> | <span data-ttu-id="70d6c-2084">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2084">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2085">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2085">Tag</span></span>   | <span data-ttu-id="70d6c-2086">0x9203</span><span class="sxs-lookup"><span data-stu-id="70d6c-2086">0x9203</span></span>                   |
| <span data-ttu-id="70d6c-2087">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2087">Type</span></span>  | <span data-ttu-id="70d6c-2088">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2088">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="70d6c-2089">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2089">Count</span></span> | <span data-ttu-id="70d6c-2090">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2090">1</span></span>                        |



 

## <a name="propertytagexifexposurebias"></a><span data-ttu-id="70d6c-2091">PropertyTagExifExposureBias</span><span class="sxs-lookup"><span data-stu-id="70d6c-2091">PropertyTagExifExposureBias</span></span>

<span data-ttu-id="70d6c-2092">暴露偏差。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2092">Exposure bias.</span></span> <span data-ttu-id="70d6c-2093">此單位為頂點值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2093">The unit is the APEX value.</span></span> <span data-ttu-id="70d6c-2094">通常會提供範圍-99.99 到99.99。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2094">Ordinarily it is given in the range -99.99 to 99.99.</span></span>



| <span data-ttu-id="70d6c-2095">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2095">Property info</span></span> | <span data-ttu-id="70d6c-2096">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2096">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2097">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2097">Tag</span></span>   | <span data-ttu-id="70d6c-2098">0x9204</span><span class="sxs-lookup"><span data-stu-id="70d6c-2098">0x9204</span></span>                   |
| <span data-ttu-id="70d6c-2099">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2099">Type</span></span>  | <span data-ttu-id="70d6c-2100">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2100">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="70d6c-2101">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2101">Count</span></span> | <span data-ttu-id="70d6c-2102">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2102">1</span></span>                        |



 

## <a name="propertytagexifmaxaperture"></a><span data-ttu-id="70d6c-2103">PropertyTagExifMaxAperture</span><span class="sxs-lookup"><span data-stu-id="70d6c-2103">PropertyTagExifMaxAperture</span></span>

<span data-ttu-id="70d6c-2104">最小的鏡頭 F 數目。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2104">Smallest F number of the lens.</span></span> <span data-ttu-id="70d6c-2105">此單位為頂點值。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2105">The unit is the APEX value.</span></span> <span data-ttu-id="70d6c-2106">通常會提供00.00 到99.99 的範圍，但不限於此範圍。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2106">Ordinarily it is given in the range of 00.00 to 99.99, but it is not limited to this range.</span></span>



| <span data-ttu-id="70d6c-2107">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2107">Property info</span></span> | <span data-ttu-id="70d6c-2108">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2108">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2109">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2109">Tag</span></span>   | <span data-ttu-id="70d6c-2110">0x9205</span><span class="sxs-lookup"><span data-stu-id="70d6c-2110">0x9205</span></span>                  |
| <span data-ttu-id="70d6c-2111">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2111">Type</span></span>  | <span data-ttu-id="70d6c-2112">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2112">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2113">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2113">Count</span></span> | <span data-ttu-id="70d6c-2114">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2114">1</span></span>                       |



 

## <a name="propertytagexifsubjectdist"></a><span data-ttu-id="70d6c-2115">PropertyTagExifSubjectDist</span><span class="sxs-lookup"><span data-stu-id="70d6c-2115">PropertyTagExifSubjectDist</span></span>

<span data-ttu-id="70d6c-2116">與主旨之間的距離，以計量測量。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2116">Distance to the subject, measured in meters.</span></span>



| <span data-ttu-id="70d6c-2117">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2117">Property info</span></span> | <span data-ttu-id="70d6c-2118">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2118">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2119">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2119">Tag</span></span>   | <span data-ttu-id="70d6c-2120">0x9206</span><span class="sxs-lookup"><span data-stu-id="70d6c-2120">0x9206</span></span>                  |
| <span data-ttu-id="70d6c-2121">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2121">Type</span></span>  | <span data-ttu-id="70d6c-2122">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2122">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2123">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2123">Count</span></span> | <span data-ttu-id="70d6c-2124">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2124">1</span></span>                       |



 

## <a name="propertytagexifmeteringmode"></a><span data-ttu-id="70d6c-2125">PropertyTagExifMeteringMode</span><span class="sxs-lookup"><span data-stu-id="70d6c-2125">PropertyTagExifMeteringMode</span></span>

<span data-ttu-id="70d6c-2126">計量模式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2126">Metering mode.</span></span>



<span data-ttu-id="70d6c-2127">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2127">Tag</span></span>

<span data-ttu-id="70d6c-2128">0x9207</span><span class="sxs-lookup"><span data-stu-id="70d6c-2128">0x9207</span></span>

<span data-ttu-id="70d6c-2129">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2129">Type</span></span>

<span data-ttu-id="70d6c-2130">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-2130">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-2131">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2131">Count</span></span>

<span data-ttu-id="70d6c-2132">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2132">1</span></span>

<span data-ttu-id="70d6c-2133">預設</span><span class="sxs-lookup"><span data-stu-id="70d6c-2133">Default</span></span>

<span data-ttu-id="70d6c-2134">0</span><span class="sxs-lookup"><span data-stu-id="70d6c-2134">0</span></span>

<span data-ttu-id="70d6c-2135">0-未知的 1-平均 2-CenterWeightedAverage 3-點 4-MultiSpot 5-模式 6-部分7到 254-保留 255-其他</span><span class="sxs-lookup"><span data-stu-id="70d6c-2135">0 - unknown 1 - Average 2 - CenterWeightedAverage 3 - Spot 4 - MultiSpot 5 - Pattern 6 - Partial 7 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexiflightsource"></a><span data-ttu-id="70d6c-2136">PropertyTagExifLightSource</span><span class="sxs-lookup"><span data-stu-id="70d6c-2136">PropertyTagExifLightSource</span></span>

<span data-ttu-id="70d6c-2137">燈光來源的類型。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2137">Type of light source.</span></span>



<span data-ttu-id="70d6c-2138">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2138">Tag</span></span>

<span data-ttu-id="70d6c-2139">0x9208</span><span class="sxs-lookup"><span data-stu-id="70d6c-2139">0x9208</span></span>

<span data-ttu-id="70d6c-2140">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2140">Type</span></span>

<span data-ttu-id="70d6c-2141">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-2141">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-2142">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2142">Count</span></span>

<span data-ttu-id="70d6c-2143">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2143">1</span></span>

<span data-ttu-id="70d6c-2144">預設</span><span class="sxs-lookup"><span data-stu-id="70d6c-2144">Default</span></span>

<span data-ttu-id="70d6c-2145">0</span><span class="sxs-lookup"><span data-stu-id="70d6c-2145">0</span></span>

<span data-ttu-id="70d6c-2146">0-未知的 1-日光 2-螢光 3-Tungsten 17-標準光 A 18-標準燈 B 19-標準燈 C 20-D55 21-D65 22-D75 23 到 254-保留 255-其他</span><span class="sxs-lookup"><span data-stu-id="70d6c-2146">0 - unknown 1 - Daylight 2 - Flourescent 3 - Tungsten 17 - Standard Light A 18 - Standard Light B 19 - Standard Light C 20 - D55 21 - D65 22 - D75 23 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexifflash"></a><span data-ttu-id="70d6c-2147">PropertyTagExifFlash</span><span class="sxs-lookup"><span data-stu-id="70d6c-2147">PropertyTagExifFlash</span></span>

<span data-ttu-id="70d6c-2148">閃爍狀態。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2148">Flash status.</span></span> <span data-ttu-id="70d6c-2149">使用明暗色亮 (flash) 來拍攝影像時，會記錄此標記。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2149">This tag is recorded when an image is taken using a strobe light (flash).</span></span> <span data-ttu-id="70d6c-2150">Bit 0 表示 flash 引發狀態，而位1和2表示 flash 傳回狀態。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2150">Bit 0 indicates the flash firing status, and bits 1 and 2 indicate the flash return status.</span></span>



<span data-ttu-id="70d6c-2151">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2151">Tag</span></span>

<span data-ttu-id="70d6c-2152">0x9209</span><span class="sxs-lookup"><span data-stu-id="70d6c-2152">0x9209</span></span>

<span data-ttu-id="70d6c-2153">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2153">Type</span></span>

<span data-ttu-id="70d6c-2154">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-2154">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-2155">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2155">Count</span></span>

<span data-ttu-id="70d6c-2156">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2156">1</span></span>

<span data-ttu-id="70d6c-2157">位0的值，指出是否已引發閃爍： 0b-閃爍未引發 1b-flash</span><span class="sxs-lookup"><span data-stu-id="70d6c-2157">Values for bit 0 that indicate whether the flash fired: 0b - flash did not fire 1b - flash fired</span></span>

<span data-ttu-id="70d6c-2158">位1和2的值，表示傳回的燈狀態： 00b-沒有閃光燈傳回偵測函式01b 每個-保留的全選色-未偵測到未偵測到的的 11b-閃光燈傳回的光線</span><span class="sxs-lookup"><span data-stu-id="70d6c-2158">Values for bits 1 and 2 that indicate the status of returned light: 00b - no strobe return detection function 01b - reserved 10b - strobe return light not detected 11b - strobe return light detected</span></span>

<span data-ttu-id="70d6c-2159">產生的閃光燈標記值： 0x0000-flash 未引發 0x0001-flash 引發的 0x0005-未偵測到明暗的傳回燈</span><span class="sxs-lookup"><span data-stu-id="70d6c-2159">Resulting flash tag values: 0x0000 - flash did not fire 0x0001 - flash fired 0x0005 - strobe return light not detected</span></span>



 

## <a name="propertytagexiffocallength"></a><span data-ttu-id="70d6c-2160">PropertyTagExifFocalLength</span><span class="sxs-lookup"><span data-stu-id="70d6c-2160">PropertyTagExifFocalLength</span></span>

<span data-ttu-id="70d6c-2161">鏡頭的實際焦點長度（以毫米為單位）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2161">Actual focal length, in millimeters, of the lens.</span></span> <span data-ttu-id="70d6c-2162">不是對35毫米膠捲攝影機的焦距進行轉換。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2162">Conversion is not made to the focal length of a 35 millimeter film camera.</span></span>



| <span data-ttu-id="70d6c-2163">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2163">Property info</span></span> | <span data-ttu-id="70d6c-2164">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2164">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2165">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2165">Tag</span></span>   | <span data-ttu-id="70d6c-2166">0x920A</span><span class="sxs-lookup"><span data-stu-id="70d6c-2166">0x920A</span></span>                  |
| <span data-ttu-id="70d6c-2167">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2167">Type</span></span>  | <span data-ttu-id="70d6c-2168">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2168">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2169">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2169">Count</span></span> | <span data-ttu-id="70d6c-2170">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2170">1</span></span>                       |



 

## <a name="propertytagexifmakernote"></a><span data-ttu-id="70d6c-2171">PropertyTagExifMakerNote</span><span class="sxs-lookup"><span data-stu-id="70d6c-2171">PropertyTagExifMakerNote</span></span>

<span data-ttu-id="70d6c-2172">附注標記。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2172">Note tag.</span></span> <span data-ttu-id="70d6c-2173">EXIF 寫入器製造商用來記錄資訊的標記。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2173">A tag used by manufacturers of EXIF writers to record information.</span></span> <span data-ttu-id="70d6c-2174">內容是由製造商所組成。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2174">The contents are up to the manufacturer.</span></span>



| <span data-ttu-id="70d6c-2175">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2175">Property info</span></span> | <span data-ttu-id="70d6c-2176">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2176">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2177">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2177">Tag</span></span>   | <span data-ttu-id="70d6c-2178">0x927C</span><span class="sxs-lookup"><span data-stu-id="70d6c-2178">0x927C</span></span>                   |
| <span data-ttu-id="70d6c-2179">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2179">Type</span></span>  | <span data-ttu-id="70d6c-2180">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-2180">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-2181">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2181">Count</span></span> | <span data-ttu-id="70d6c-2182">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-2182">Any</span></span>                      |



 

## <a name="propertytagexifusercomment"></a><span data-ttu-id="70d6c-2183">PropertyTagExifUserComment</span><span class="sxs-lookup"><span data-stu-id="70d6c-2183">PropertyTagExifUserComment</span></span>

<span data-ttu-id="70d6c-2184">註解標記。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2184">Comment tag.</span></span> <span data-ttu-id="70d6c-2185">由 EXIF 使用者用來寫入影像的關鍵字或批註的標籤，除了在 PropertyTagImageDescription 中，以及沒有 PropertyTagImageDescription 標記的字元碼限制之外。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2185">A tag used by EXIF users to write keywords or comments about the image besides those in PropertyTagImageDescription and without the character-code limitations of the PropertyTagImageDescription tag.</span></span>



| <span data-ttu-id="70d6c-2186">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2186">Property info</span></span> | <span data-ttu-id="70d6c-2187">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2187">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2188">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2188">Tag</span></span>   | <span data-ttu-id="70d6c-2189">0x9286</span><span class="sxs-lookup"><span data-stu-id="70d6c-2189">0x9286</span></span>                   |
| <span data-ttu-id="70d6c-2190">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2190">Type</span></span>  | <span data-ttu-id="70d6c-2191">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-2191">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-2192">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2192">Count</span></span> | <span data-ttu-id="70d6c-2193">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-2193">Any</span></span>                      |



 

<span data-ttu-id="70d6c-2194">PropertyTagExifUserComment 標籤中使用的字元碼是根據標記資料區域開頭固定8位元組區域中的識別碼碼來識別。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2194">The character code used in the PropertyTagExifUserComment tag is identified based on an ID code in a fixed 8-byte area at the start of the tag data area.</span></span> <span data-ttu-id="70d6c-2195">區域未使用的部分會以 null 字元填補 (0) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2195">The unused portion of the area is padded with null characters (0).</span></span> <span data-ttu-id="70d6c-2196">識別碼代碼是透過註冊方式來指派。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2196">ID codes are assigned by means of registration.</span></span> <span data-ttu-id="70d6c-2197">因為類型不是 ASCII，所以不需要使用 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2197">Because the type is not ASCII, it is not necessary to use a NULL terminator.</span></span>

## <a name="propertytagexifdtsubsec"></a><span data-ttu-id="70d6c-2198">PropertyTagExifDTSubsec</span><span class="sxs-lookup"><span data-stu-id="70d6c-2198">PropertyTagExifDTSubsec</span></span>

<span data-ttu-id="70d6c-2199">以 Null 結束的字元字串，指定 PropertyTagDateTime 標記的第二個部分。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2199">Null-terminated character string that specifies a fraction of a second for the PropertyTagDateTime tag.</span></span>



| <span data-ttu-id="70d6c-2200">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2200">Property info</span></span> | <span data-ttu-id="70d6c-2201">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2201">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="70d6c-2202">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2202">Tag</span></span>   | <span data-ttu-id="70d6c-2203">0x9290</span><span class="sxs-lookup"><span data-stu-id="70d6c-2203">0x9290</span></span>                                             |
| <span data-ttu-id="70d6c-2204">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2204">Type</span></span>  | <span data-ttu-id="70d6c-2205">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-2205">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-2206">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2206">Count</span></span> | <span data-ttu-id="70d6c-2207">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-2207">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtorigss"></a><span data-ttu-id="70d6c-2208">PropertyTagExifDTOrigSS</span><span class="sxs-lookup"><span data-stu-id="70d6c-2208">PropertyTagExifDTOrigSS</span></span>

<span data-ttu-id="70d6c-2209">以 Null 結束的字元字串，指定 PropertyTagExifDTOrig 標記的第二個部分。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2209">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTOrig tag.</span></span>



| <span data-ttu-id="70d6c-2210">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2210">Property info</span></span> | <span data-ttu-id="70d6c-2211">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2211">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="70d6c-2212">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2212">Tag</span></span>  | <span data-ttu-id="70d6c-2213">0x9291</span><span class="sxs-lookup"><span data-stu-id="70d6c-2213">0x9291</span></span>                                             |
| <span data-ttu-id="70d6c-2214">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2214">Type</span></span> | <span data-ttu-id="70d6c-2215">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-2215">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="70d6c-2216">N</span><span class="sxs-lookup"><span data-stu-id="70d6c-2216">N</span></span>    | <span data-ttu-id="70d6c-2217">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-2217">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtdigss"></a><span data-ttu-id="70d6c-2218">PropertyTagExifDTDigSS</span><span class="sxs-lookup"><span data-stu-id="70d6c-2218">PropertyTagExifDTDigSS</span></span>

<span data-ttu-id="70d6c-2219">以 Null 結束的字元字串，指定 PropertyTagExifDTDigitized 標記的第二個部分。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2219">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTDigitized tag.</span></span>



| <span data-ttu-id="70d6c-2220">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2220">Property info</span></span> | <span data-ttu-id="70d6c-2221">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2221">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="70d6c-2222">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2222">Tag</span></span>  | <span data-ttu-id="70d6c-2223">0x9292</span><span class="sxs-lookup"><span data-stu-id="70d6c-2223">0x9292</span></span>                                             |
| <span data-ttu-id="70d6c-2224">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2224">Type</span></span> | <span data-ttu-id="70d6c-2225">ASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-2225">ASCII</span></span>                                              |
| <span data-ttu-id="70d6c-2226">N</span><span class="sxs-lookup"><span data-stu-id="70d6c-2226">N</span></span>    | <span data-ttu-id="70d6c-2227">字串的長度，包括 Null 結束字元</span><span class="sxs-lookup"><span data-stu-id="70d6c-2227">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexiffpxver"></a><span data-ttu-id="70d6c-2228">PropertyTagExifFPXVer</span><span class="sxs-lookup"><span data-stu-id="70d6c-2228">PropertyTagExifFPXVer</span></span>

<span data-ttu-id="70d6c-2229">FPXR 檔案支援的 FlashPix 格式版本。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2229">FlashPix format version supported by an FPXR file.</span></span> <span data-ttu-id="70d6c-2230">如果 FPXR 函式支援 FlashPix 格式版本1.0，則會以4位元組 ASCII 字串的形式錄製0100，以類似 PropertyTagExifVer 的方式來表示。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2230">If the FPXR function supports FlashPix format version 1.0, this is indicated similarly to PropertyTagExifVer by recording 0100 as a 4-byte ASCII string.</span></span> <span data-ttu-id="70d6c-2231">因為類型是 PropertyTagTypeUndefined，所以沒有 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2231">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



<span data-ttu-id="70d6c-2232">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2232">Tag</span></span>

<span data-ttu-id="70d6c-2233">0xA000</span><span class="sxs-lookup"><span data-stu-id="70d6c-2233">0xA000</span></span>

<span data-ttu-id="70d6c-2234">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2234">Type</span></span>

<span data-ttu-id="70d6c-2235">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-2235">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="70d6c-2236">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2236">Count</span></span>

<span data-ttu-id="70d6c-2237">4</span><span class="sxs-lookup"><span data-stu-id="70d6c-2237">4</span></span>

<span data-ttu-id="70d6c-2238">預設</span><span class="sxs-lookup"><span data-stu-id="70d6c-2238">Default</span></span>

<span data-ttu-id="70d6c-2239">0100</span><span class="sxs-lookup"><span data-stu-id="70d6c-2239">0100</span></span>

<span data-ttu-id="70d6c-2240">0100-FlashPix format version 1.0 Other-reserved</span><span class="sxs-lookup"><span data-stu-id="70d6c-2240">0100 - FlashPix format version 1.0 Other - reserved</span></span>



 

## <a name="propertytagexifcolorspace"></a><span data-ttu-id="70d6c-2241">PropertyTagExifColorSpace</span><span class="sxs-lookup"><span data-stu-id="70d6c-2241">PropertyTagExifColorSpace</span></span>

<span data-ttu-id="70d6c-2242">色彩空間規範。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2242">Color space specifier.</span></span> <span data-ttu-id="70d6c-2243">通常是使用 sRGB (= 1) ，根據電腦監視器的狀況和環境定義色彩空間。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2243">Normally sRGB (=1) is used to define the color space based on the PC monitor conditions and environment.</span></span> <span data-ttu-id="70d6c-2244">如果使用 sRGB 以外的色彩空間，則會設定 Uncalibrated (= 0xFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2244">If a color space other than sRGB is used, Uncalibrated (=0xFFFF) is set.</span></span> <span data-ttu-id="70d6c-2245">記錄為 Uncalibrated 的影像資料在轉換成 FlashPix 時，可以視為 sRGB。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2245">Image data recorded as Uncalibrated can be treated as sRGB when it is converted to FlashPix.</span></span>



<span data-ttu-id="70d6c-2246">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2246">Tag</span></span>

<span data-ttu-id="70d6c-2247">0xA001</span><span class="sxs-lookup"><span data-stu-id="70d6c-2247">0xA001</span></span>

<span data-ttu-id="70d6c-2248">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2248">Type</span></span>

<span data-ttu-id="70d6c-2249">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-2249">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-2250">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2250">Count</span></span>

<span data-ttu-id="70d6c-2251">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2251">1</span></span>

<span data-ttu-id="70d6c-2252">0x1-sRGB 0xFFFF-uncalibrated 其他-保留</span><span class="sxs-lookup"><span data-stu-id="70d6c-2252">0x1 - sRGB 0xFFFF - uncalibrated Other - reserved</span></span>



 

## <a name="propertytagexifpixxdim"></a><span data-ttu-id="70d6c-2253">PropertyTagExifPixXDim</span><span class="sxs-lookup"><span data-stu-id="70d6c-2253">PropertyTagExifPixXDim</span></span>

<span data-ttu-id="70d6c-2254">壓縮資料的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2254">Information specific to compressed data.</span></span> <span data-ttu-id="70d6c-2255">當記錄了壓縮檔案時，無論是否有填補資料或重新開機標記，都必須在此標記中記錄有意義之影像的有效寬度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2255">When a compressed file is recorded, the valid width of the meaningful image must be recorded in this tag, whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="70d6c-2256">此標記不應該存在於未壓縮檔案中。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2256">This tag should not exist in an uncompressed file.</span></span>



| <span data-ttu-id="70d6c-2257">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2257">Property info</span></span> | <span data-ttu-id="70d6c-2258">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2258">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-2259">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2259">Tag</span></span>   | <span data-ttu-id="70d6c-2260">0xA002</span><span class="sxs-lookup"><span data-stu-id="70d6c-2260">0xA002</span></span>                                      |
| <span data-ttu-id="70d6c-2261">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2261">Type</span></span>  | <span data-ttu-id="70d6c-2262">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-2262">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-2263">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2263">Count</span></span> | <span data-ttu-id="70d6c-2264">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2264">1</span></span>                                           |



 

## <a name="propertytagexifpixydim"></a><span data-ttu-id="70d6c-2265">PropertyTagExifPixYDim</span><span class="sxs-lookup"><span data-stu-id="70d6c-2265">PropertyTagExifPixYDim</span></span>

<span data-ttu-id="70d6c-2266">壓縮資料的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2266">Information specific to compressed data.</span></span> <span data-ttu-id="70d6c-2267">當記錄了壓縮檔案時，無論是否有填補資料或重新開機標記，都必須在此標記中記錄有意義之影像的有效高度。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2267">When a compressed file is recorded, the valid height of the meaningful image must be recorded in this tag whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="70d6c-2268">此標記不應該存在於未壓縮檔案中。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2268">This tag should not exist in an uncompressed file.</span></span> <span data-ttu-id="70d6c-2269">因為垂直方向不需要資料填補，所以在此有效影像高度標記中錄製的行數將與 t 中記錄的行數相同。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2269">Because data padding is unnecessary in the vertical direction, the number of lines recorded in this valid image height tag will be the same as that recorded in the SOF.</span></span>



| <span data-ttu-id="70d6c-2270">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2270">Property info</span></span> | <span data-ttu-id="70d6c-2271">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2271">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="70d6c-2272">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2272">Tag</span></span>   | <span data-ttu-id="70d6c-2273">0xA003</span><span class="sxs-lookup"><span data-stu-id="70d6c-2273">0xA003</span></span>                                      |
| <span data-ttu-id="70d6c-2274">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2274">Type</span></span>  | <span data-ttu-id="70d6c-2275">PropertyTagTypeShort 或 PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-2275">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-2276">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2276">Count</span></span> | <span data-ttu-id="70d6c-2277">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2277">1</span></span>                                           |



 

## <a name="propertytagexifrelatedwav"></a><span data-ttu-id="70d6c-2278">PropertyTagExifRelatedWav</span><span class="sxs-lookup"><span data-stu-id="70d6c-2278">PropertyTagExifRelatedWav</span></span>

<span data-ttu-id="70d6c-2279">與影像資料相關的音訊檔案名。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2279">The name of an audio file related to the image data.</span></span> <span data-ttu-id="70d6c-2280">唯一記錄的關聯式資訊是 EXIF 音訊檔案名和副檔名， (包含8個字元加上句號 ( 的 ASCII 字串。 ) ，再加上3個字元) 。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2280">The only relational information recorded is the EXIF audio file name and extension (an ASCII string that consists of 8 characters plus a period (.), plus 3 characters).</span></span> <span data-ttu-id="70d6c-2281">不會記錄路徑。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2281">The path is not recorded.</span></span> <span data-ttu-id="70d6c-2282">當您使用此標記時，必須記錄音訊檔案，且必須符合 EXIF 音訊格式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2282">When you use this tag, audio files must be recorded in conformance with the EXIF audio format.</span></span> <span data-ttu-id="70d6c-2283">寫入器也可以將 APP2 中的音訊資料儲存為 FlashPix 擴充資料流程資料。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2283">Writers can also store audio data within APP2 as FlashPix extension stream data.</span></span>



| <span data-ttu-id="70d6c-2284">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2284">Property info</span></span> | <span data-ttu-id="70d6c-2285">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2285">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-2286">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2286">Tag</span></span>   | <span data-ttu-id="70d6c-2287">0xA004</span><span class="sxs-lookup"><span data-stu-id="70d6c-2287">0xA004</span></span>               |
| <span data-ttu-id="70d6c-2288">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2288">Type</span></span>  | <span data-ttu-id="70d6c-2289">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="70d6c-2289">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="70d6c-2290">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2290">Count</span></span> | <span data-ttu-id="70d6c-2291">13</span><span class="sxs-lookup"><span data-stu-id="70d6c-2291">13</span></span>                   |



 

## <a name="propertytagexifinterop"></a><span data-ttu-id="70d6c-2292">PropertyTagExifInterop</span><span class="sxs-lookup"><span data-stu-id="70d6c-2292">PropertyTagExifInterop</span></span>

<span data-ttu-id="70d6c-2293">包含互通性資訊的屬性專案區塊的位移。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2293">Offset to a block of property items that contain interoperability information.</span></span>



| <span data-ttu-id="70d6c-2294">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2294">Property info</span></span> | <span data-ttu-id="70d6c-2295">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2295">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="70d6c-2296">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2296">Tag</span></span>   | <span data-ttu-id="70d6c-2297">0xA005</span><span class="sxs-lookup"><span data-stu-id="70d6c-2297">0xA005</span></span>              |
| <span data-ttu-id="70d6c-2298">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2298">Type</span></span>  | <span data-ttu-id="70d6c-2299">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="70d6c-2299">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="70d6c-2300">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2300">Count</span></span> | <span data-ttu-id="70d6c-2301">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2301">1</span></span>                   |



 

## <a name="propertytagexifflashenergy"></a><span data-ttu-id="70d6c-2302">PropertyTagExifFlashEnergy</span><span class="sxs-lookup"><span data-stu-id="70d6c-2302">PropertyTagExifFlashEnergy</span></span>

<span data-ttu-id="70d6c-2303">在捕獲映射時， (BCPS) 的閃光燈能源（以橫樑為單位）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2303">Strobe energy, in Beam Candle Power Seconds (BCPS), at the time the image was captured.</span></span>



| <span data-ttu-id="70d6c-2304">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2304">Property info</span></span> | <span data-ttu-id="70d6c-2305">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2306">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2306">Tag</span></span>   | <span data-ttu-id="70d6c-2307">0xA20B</span><span class="sxs-lookup"><span data-stu-id="70d6c-2307">0xA20B</span></span>                  |
| <span data-ttu-id="70d6c-2308">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2308">Type</span></span>  | <span data-ttu-id="70d6c-2309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2310">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2310">Count</span></span> | <span data-ttu-id="70d6c-2311">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2311">1</span></span>                       |



 

## <a name="propertytagexifspatialfr"></a><span data-ttu-id="70d6c-2312">PropertyTagExifSpatialFR</span><span class="sxs-lookup"><span data-stu-id="70d6c-2312">PropertyTagExifSpatialFR</span></span>

<span data-ttu-id="70d6c-2313">攝影機或輸入裝置空間頻率表，以及影像寬度、影像高度和對角線方向的 SFR. 值（如 ISO 12233 中所指定）。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2313">Camera or input device spatial frequency table and SFR values in the image width, image height, and diagonal direction, as specified in ISO 12233.</span></span>



| <span data-ttu-id="70d6c-2314">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2314">Property info</span></span> | <span data-ttu-id="70d6c-2315">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2315">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2316">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2316">Tag</span></span>   | <span data-ttu-id="70d6c-2317">0xA20C</span><span class="sxs-lookup"><span data-stu-id="70d6c-2317">0xA20C</span></span>                   |
| <span data-ttu-id="70d6c-2318">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2318">Type</span></span>  | <span data-ttu-id="70d6c-2319">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-2319">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-2320">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2320">Count</span></span> | <span data-ttu-id="70d6c-2321">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-2321">Any</span></span>                      |



 

## <a name="propertytagexiffocalxres"></a><span data-ttu-id="70d6c-2322">PropertyTagExifFocalXRes</span><span class="sxs-lookup"><span data-stu-id="70d6c-2322">PropertyTagExifFocalXRes</span></span>

<span data-ttu-id="70d6c-2323">影像寬度的圖元數， (相機焦點平面上每個單位的 x) 方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2323">Number of pixels in the image width (x) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="70d6c-2324">單位是在 PropertyTagExifFocalResUnit 中指定。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2324">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="70d6c-2325">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2325">Property info</span></span> | <span data-ttu-id="70d6c-2326">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2326">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2327">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2327">Tag</span></span>   | <span data-ttu-id="70d6c-2328">0xA20E</span><span class="sxs-lookup"><span data-stu-id="70d6c-2328">0xA20E</span></span>                  |
| <span data-ttu-id="70d6c-2329">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2329">Type</span></span>  | <span data-ttu-id="70d6c-2330">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2330">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2331">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2331">Count</span></span> | <span data-ttu-id="70d6c-2332">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2332">1</span></span>                       |



 

## <a name="propertytagexiffocalyres"></a><span data-ttu-id="70d6c-2333">PropertyTagExifFocalYRes</span><span class="sxs-lookup"><span data-stu-id="70d6c-2333">PropertyTagExifFocalYRes</span></span>

<span data-ttu-id="70d6c-2334">影像高度中的圖元數 (y) 相機焦點平面上每個單位的方向。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2334">Number of pixels in the image height (y) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="70d6c-2335">單位是在 PropertyTagExifFocalResUnit 中指定。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2335">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="70d6c-2336">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2336">Property info</span></span> | <span data-ttu-id="70d6c-2337">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2337">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2338">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2338">Tag</span></span>   | <span data-ttu-id="70d6c-2339">0xA20F</span><span class="sxs-lookup"><span data-stu-id="70d6c-2339">0xA20F</span></span>                  |
| <span data-ttu-id="70d6c-2340">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2340">Type</span></span>  | <span data-ttu-id="70d6c-2341">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2341">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2342">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2342">Count</span></span> | <span data-ttu-id="70d6c-2343">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2343">1</span></span>                       |



 

## <a name="propertytagexiffocalresunit"></a><span data-ttu-id="70d6c-2344">PropertyTagExifFocalResUnit</span><span class="sxs-lookup"><span data-stu-id="70d6c-2344">PropertyTagExifFocalResUnit</span></span>

<span data-ttu-id="70d6c-2345">PropertyTagExifFocalXRes 和 PropertyTagExifFocalYRes 的測量單位。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2345">Unit of measure for PropertyTagExifFocalXRes and PropertyTagExifFocalYRes.</span></span>



<span data-ttu-id="70d6c-2346">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2346">Tag</span></span>

<span data-ttu-id="70d6c-2347">0xA210</span><span class="sxs-lookup"><span data-stu-id="70d6c-2347">0xA210</span></span>

<span data-ttu-id="70d6c-2348">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2348">Type</span></span>

<span data-ttu-id="70d6c-2349">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-2349">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-2350">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2350">Count</span></span>

<span data-ttu-id="70d6c-2351">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2351">1</span></span>

<span data-ttu-id="70d6c-2352">2-英寸 3-釐米</span><span class="sxs-lookup"><span data-stu-id="70d6c-2352">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagexifsubjectloc"></a><span data-ttu-id="70d6c-2353">PropertyTagExifSubjectLoc</span><span class="sxs-lookup"><span data-stu-id="70d6c-2353">PropertyTagExifSubjectLoc</span></span>

<span data-ttu-id="70d6c-2354">場景中主體的位置。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2354">Location of the main subject in the scene.</span></span> <span data-ttu-id="70d6c-2355">此標記的值代表主要主體相對於左邊緣的圖元。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2355">The value of this tag represents the pixel at the center of the main subject relative to the left edge.</span></span> <span data-ttu-id="70d6c-2356">第一個值表示資料行編號，而第二個值表示資料列編號。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2356">The first value indicates the column number, and the second value indicates the row number.</span></span>



| <span data-ttu-id="70d6c-2357">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2357">Property info</span></span> | <span data-ttu-id="70d6c-2358">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2358">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="70d6c-2359">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2359">Tag</span></span>   | <span data-ttu-id="70d6c-2360">0xA214</span><span class="sxs-lookup"><span data-stu-id="70d6c-2360">0xA214</span></span>               |
| <span data-ttu-id="70d6c-2361">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2361">Type</span></span>  | <span data-ttu-id="70d6c-2362">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-2362">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="70d6c-2363">計數</span><span class="sxs-lookup"><span data-stu-id="70d6c-2363">Count</span></span> | <span data-ttu-id="70d6c-2364">2</span><span class="sxs-lookup"><span data-stu-id="70d6c-2364">2</span></span>                    |



 

## <a name="propertytagexifexposureindex"></a><span data-ttu-id="70d6c-2365">PropertyTagExifExposureIndex</span><span class="sxs-lookup"><span data-stu-id="70d6c-2365">PropertyTagExifExposureIndex</span></span>

<span data-ttu-id="70d6c-2366">在拍攝映射時，于相機或輸入裝置上選取的公開索引。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2366">Exposure index selected on the camera or input device at the time the image was captured.</span></span>



| <span data-ttu-id="70d6c-2367">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2367">Property info</span></span> | <span data-ttu-id="70d6c-2368">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2368">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="70d6c-2369">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2369">Tag</span></span>   | <span data-ttu-id="70d6c-2370">0xA215</span><span class="sxs-lookup"><span data-stu-id="70d6c-2370">0xA215</span></span>                  |
| <span data-ttu-id="70d6c-2371">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2371">Type</span></span>  | <span data-ttu-id="70d6c-2372">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="70d6c-2372">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="70d6c-2373">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2373">Count</span></span> | <span data-ttu-id="70d6c-2374">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2374">1</span></span>                       |



 

## <a name="propertytagexifsensingmethod"></a><span data-ttu-id="70d6c-2375">PropertyTagExifSensingMethod</span><span class="sxs-lookup"><span data-stu-id="70d6c-2375">PropertyTagExifSensingMethod</span></span>

<span data-ttu-id="70d6c-2376">相機或輸入裝置上的影像感應器類型。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2376">Image sensor type on the camera or input device.</span></span>



<span data-ttu-id="70d6c-2377">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2377">Tag</span></span>

<span data-ttu-id="70d6c-2378">0xA217</span><span class="sxs-lookup"><span data-stu-id="70d6c-2378">0xA217</span></span>

<span data-ttu-id="70d6c-2379">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2379">Type</span></span>

<span data-ttu-id="70d6c-2380">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="70d6c-2380">PropertyTagTypeShort</span></span>

<span data-ttu-id="70d6c-2381">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2381">Count</span></span>

<span data-ttu-id="70d6c-2382">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2382">1</span></span>

<span data-ttu-id="70d6c-2383">1-未定義 2-一晶片色彩區域感應器 3-雙晶片色彩區域感應器 4-三晶片色彩區域感應器 5-彩色順序區域感應器 7-色彩順序區域感應器 7-三線性感應器 8-色彩順序線性感應器（其他-保留）</span><span class="sxs-lookup"><span data-stu-id="70d6c-2383">1 - not defined 2 - one-chip color area sensor 3 - two-chip color area sensor 4 - three-chip color area sensor 5 - color sequential area sensor 7 - trilinear sensor 8 - color sequential linear sensor Other - reserved</span></span>



 

## <a name="propertytagexiffilesource"></a><span data-ttu-id="70d6c-2384">PropertyTagExifFileSource</span><span class="sxs-lookup"><span data-stu-id="70d6c-2384">PropertyTagExifFileSource</span></span>

<span data-ttu-id="70d6c-2385">影像來源。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2385">The image source.</span></span> <span data-ttu-id="70d6c-2386">如果 DSC 錄製了映射，則此標記的值為3。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2386">If a DSC recorded the image, the value of this tag is 3.</span></span>



| <span data-ttu-id="70d6c-2387">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2387">Property info</span></span> | <span data-ttu-id="70d6c-2388">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2388">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2389">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2389">Tag</span></span>   | <span data-ttu-id="70d6c-2390">0xA300</span><span class="sxs-lookup"><span data-stu-id="70d6c-2390">0xA300</span></span>                   |
| <span data-ttu-id="70d6c-2391">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2391">Type</span></span>  | <span data-ttu-id="70d6c-2392">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-2392">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-2393">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2393">Count</span></span> | <span data-ttu-id="70d6c-2394">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2394">1</span></span>                        |



 

## <a name="propertytagexifscenetype"></a><span data-ttu-id="70d6c-2395">PropertyTagExifSceneType</span><span class="sxs-lookup"><span data-stu-id="70d6c-2395">PropertyTagExifSceneType</span></span>

<span data-ttu-id="70d6c-2396">場景的型別。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2396">The type of scene.</span></span> <span data-ttu-id="70d6c-2397">如果 DSC 錄製了映射，此標記的值必須設定為1，表示已直接拍攝映射。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2397">If a DSC recorded the image, the value of this tag must be set to 1, indicating that the image was directly photographed.</span></span>



| <span data-ttu-id="70d6c-2398">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2398">Property info</span></span> | <span data-ttu-id="70d6c-2399">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2399">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2400">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2400">Tag</span></span>   | <span data-ttu-id="70d6c-2401">0xA301</span><span class="sxs-lookup"><span data-stu-id="70d6c-2401">0xA301</span></span>                   |
| <span data-ttu-id="70d6c-2402">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2402">Type</span></span>  | <span data-ttu-id="70d6c-2403">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-2403">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-2404">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2404">Count</span></span> | <span data-ttu-id="70d6c-2405">1</span><span class="sxs-lookup"><span data-stu-id="70d6c-2405">1</span></span>                        |



 

## <a name="propertytagexifcfapattern"></a><span data-ttu-id="70d6c-2406">PropertyTagExifCfaPattern</span><span class="sxs-lookup"><span data-stu-id="70d6c-2406">PropertyTagExifCfaPattern</span></span>

<span data-ttu-id="70d6c-2407">色彩篩選器陣列 (使用單一晶片色彩區域感應器時，共同體影像感應器) 幾何模式。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2407">The color filter array (CFA) geometric pattern of the image sensor when a one-chip color area sensor is used.</span></span> <span data-ttu-id="70d6c-2408">它並不適用于所有的檢測方法。</span><span class="sxs-lookup"><span data-stu-id="70d6c-2408">It does not apply to all sensing methods.</span></span>



| <span data-ttu-id="70d6c-2409">屬性資訊</span><span class="sxs-lookup"><span data-stu-id="70d6c-2409">Property info</span></span> | <span data-ttu-id="70d6c-2410">值</span><span class="sxs-lookup"><span data-stu-id="70d6c-2410">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="70d6c-2411">標籤</span><span class="sxs-lookup"><span data-stu-id="70d6c-2411">Tag</span></span>   | <span data-ttu-id="70d6c-2412">0xA302</span><span class="sxs-lookup"><span data-stu-id="70d6c-2412">0xA302</span></span>                   |
| <span data-ttu-id="70d6c-2413">類型</span><span class="sxs-lookup"><span data-stu-id="70d6c-2413">Type</span></span>  | <span data-ttu-id="70d6c-2414">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="70d6c-2414">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="70d6c-2415">Count</span><span class="sxs-lookup"><span data-stu-id="70d6c-2415">Count</span></span> | <span data-ttu-id="70d6c-2416">任意</span><span class="sxs-lookup"><span data-stu-id="70d6c-2416">Any</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="70d6c-2417">相關主題</span><span class="sxs-lookup"><span data-stu-id="70d6c-2417">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70d6c-2418">影像檔案格式規格</span><span class="sxs-lookup"><span data-stu-id="70d6c-2418">Image File Format Specifications</span></span>](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[<span data-ttu-id="70d6c-2419">影像屬性標記常數</span><span class="sxs-lookup"><span data-stu-id="70d6c-2419">Image Property Tag Constants</span></span>](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[<span data-ttu-id="70d6c-2420">**影像屬性標記類型常數**</span><span class="sxs-lookup"><span data-stu-id="70d6c-2420">**Image Property Tag Type Constants**</span></span>](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[<span data-ttu-id="70d6c-2421">依字母順序排列的屬性標記</span><span class="sxs-lookup"><span data-stu-id="70d6c-2421">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[<span data-ttu-id="70d6c-2422">以數位順序排序的屬性標記</span><span class="sxs-lookup"><span data-stu-id="70d6c-2422">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[<span data-ttu-id="70d6c-2423">讀取和寫入中繼資料</span><span class="sxs-lookup"><span data-stu-id="70d6c-2423">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



